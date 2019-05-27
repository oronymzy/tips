# replacing a string in multiple files
## 1. Replacing all occurrences of one string with another in all files in the current directory:

These are for cases where you *know* that the directory contains only regular files and that you want to process all non-hidden files. If that is not the case, use the approaches in 2.

All `sed` solutions in this answer assume GNU `sed`. If using FreeBSD or OS/X, replace `-i` with `-i ''`. Also note that the use of the `-i` switch with any version of `sed` has certain filesystem [security implications](http://lists.gnu.org/archive/html/bug-gnu-utils/2013-09/msg00000.html) and is inadvisable in any script which you plan to distribute in any way.

- Non recursive, files in this directory only:
    
    ```
    sed -i -- 's/foo/bar/g' *
    perl -i -pe 's/foo/bar/g' ./*
    ```
    
    (the [`perl` one will fail for file names ending in `|` or space](https://unix.stackexchange.com/q/170013/22565)).

- Recursive, regular files (**including hidden ones**) in this and all subdirectories

    `find . -type f -exec sed -i 's/foo/bar/g' {} +`

    If you are using zsh:

    `sed -i -- 's/foo/bar/g' **/*(D.)`

    (may fail if the list is too big, see `zargs` to work around).

    Bash can't check directly for regular files, a loop is needed (braces avoid setting the options globally):

    ```
    ( shopt -s globstar dotglob;
        for file in **; do
            if [[ -f $file ]] && [[ -w $file ]]; then
                sed -i -- 's/foo/bar/g' "$file"
            fi
        done
    )
    ```

    The files are selected when they are actual files (-f) and they are writable (-w).

## 2. Replace only if the file name matches another string / has a specific extension / is of a certain type etc:

- Non-recursive, files in this directory only:

    ```
    sed -i -- 's/foo/bar/g' *baz*    ## all files whose name contains baz
    sed -i -- 's/foo/bar/g' *.baz    ## files ending in .baz
    ```

- Recursive, regular files in this and all subdirectories

    `find . -type f -name "*baz*" -exec sed -i 's/foo/bar/g' {} +`

    If you are using bash (braces avoid setting the options globally):

    ```
    ( shopt -s globstar dotglob
        sed -i -- 's/foo/bar/g' **baz*
        sed -i -- 's/foo/bar/g' **.baz
    )
    ```

    If you are using zsh:

    ```
    sed -i -- 's/foo/bar/g' **/*baz*(D.)
    sed -i -- 's/foo/bar/g' **/*.baz(D.)
    ```

    The `--` serves to tell `sed` that no more flags will be given in the command line. This is useful to protect against file names starting with `-`.

- If a file is of a certain type, for example, executable (see `man find` for more options):

    `find . -type f -executable -exec sed -i 's/foo/bar/g' {} +`

    `zsh`:

    `sed -i -- 's/foo/bar/g' **/*(D*)`


## 3. Replace only if the string is found in a certain context

- Replace `foo` with `bar` only if there is a `baz` later on the same line:

    `sed -i 's/foo\(.*baz\)/bar\1/' file`

    In `sed`, using `\( \)` saves whatever is in the parentheses and you can then access it with `\1`. There are many variations of this theme, to learn more about such regular expressions, see [here](http://www.regular-expressions.info/). 

- Replace `foo` with `bar` only if `foo` is found on the 3d column (field) of the input file (assuming whitespace-separated fields):

    `gawk -i inplace '{gsub(/foo/,"baz",$3); print}' file`

    (needs `gawk` 4.1.0 or newer).

- For a different field just use `$N` where `N` is the number of the field of interest. For a different field separator (`:` in this example) use:

    `gawk -i inplace -F':' '{gsub(/foo/,"baz",$3);print}' file`

    Another solution using `perl`:

    `perl -i -ane '$F[2]=~s/foo/baz/g; $" = " "; print "@F\n"' foo` 

    !!! note
        
        Both the `awk` and `perl` solutions will affect spacing in the file (remove the leading and trailing blanks, and convert sequences of blanks to one space character in those lines that match). For a different field, use `$F[N-1]` where `N` is the field number you want and for a different field separator use (the `$"=":"` sets the output field separator to `:`):
        
        `perl -i -F':' -ane '$F[2]=~s/foo/baz/g; $"=":";print "@F"' foo`

- Replace `foo` with `bar` only on the 4th line:

    ```
    sed -i '4s/foo/bar/g' file
    gawk -i inplace 'NR==4{gsub(/foo/,"baz")};1' file
    perl -i -pe 's/foo/bar/g if $.==4' file
    ```

## 4. Multiple replace operations: replace with different strings

- You can combine `sed` commands:

    `sed -i 's/foo/bar/g; s/baz/zab/g; s/Alice/Joan/g' file`

    Be aware that order matters (`sed 's/foo/bar/g; s/bar/baz/g'` will substitute `foo` with `baz`).

- or Perl commands
 
    `perl -i -pe 's/foo/bar/g; s/baz/zab/g; s/Alice/Joan/g' file`

- If you have a large number of patterns, it is easier to save your patterns and their replacements in a `sed` script file:

    ```
    #! /usr/bin/sed -f
    s/foo/bar/g
    s/baz/zab/g
    ```

- Or, if you have too many pattern pairs for the above to be feasible, you can read pattern pairs from a file (two space separated patterns, $pattern and $replacement, per line):

    ```
    while read -r pattern replacement; do   
        sed -i "s/$pattern/$replacement/" file
    done < patterns.txt
    ```

- That will be quite slow for long lists of patterns and large data files so you might want to read the patterns and create a `sed` script from them instead. The following assumes a *<<!>space<!>>* delimiter separates a list of *MATCH<<!>space<!>>REPLACE* pairs occurring one-per-line in the file *`patterns.txt`* :

    ```
    sed 's| *\([^ ]*\) *\([^ ]*\).*|s/\1/\2/g|' <patterns.txt |
    sed -f- ./editfile >outfile
    ```

    The above format is largely arbitrary and, for example, doesn't allow for a *<<!>space<!>>* in either of *MATCH* or *REPLACE*. The method is very general though: basically, if you can create an output stream which looks like a `sed` script, then you can source that stream as a `sed` script by specifying `sed`'s script file as `-` stdin.

- You can combine and concatenate multiple scripts in similar fashion:

    ```
    SOME_PIPELINE |
    sed -e'#some expression script'  \
        -f./script_file -f-          \
        -e'#more inline expressions' \
    ./actual_edit_file >./outfile
    ```

    A POSIX `sed` will concatenate all scripts into one in the order they appear on the command-line. None of these need end in a `\n`ewline.

- `grep` can work the same way:

    ```
    sed -e'#generate a pattern list' <in |
    grep -f- ./grepped_file
    ```

- When working with fixed-strings as patterns, it is good practice to escape regular expression *metacharacters*. You can do this rather easily:

    ```
    sed 's/[]$&^*\./[]/\\&/g
        s| *\([^ ]*\) *\([^ ]*\).*|s/\1/\2/g|
    ' <patterns.txt |
    sed -f- ./editfile >outfile
    ```

## 5. Multiple replace operations: replace multiple patterns with the same string

- Replace any of `foo`, `bar` or `baz` with `foobar`

    `sed -Ei 's/foo|bar|baz/foobar/g' file`

- or

    `perl -i -pe 's/foo|bar|baz/foobar/g' file`

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Stack Exchange by community wiki](https://unix.stackexchange.com/questions/112023/how-can-i-replace-a-string-in-a-files/112024#112024), with changes made.
