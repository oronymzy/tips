# installing [Jekyll]

??? info "Personal experience"
    
    Tested in Kubuntu 17.10.

Jekyll requires [Ruby](https://en.wikipedia.org/wiki/Ruby_(programming_language)), [RubyGems](https://en.wikipedia.org/wiki/RubyGems), [GCC](https://en.wikipedia.org/wiki/GNU_Compiler_Collection), and [Make](https://www.gnu.org/software/make/). In Ubuntu, [install the Ruby Version Manager](insRVMr.md), then open Gnome Terminal with `gnome-terminal`. Use `rvm list` to check if Ruby version 2.1 or greater is installed, and if not use `rvm install ruby`. Verify RubyGems is installed with `gem -v`, GCC is installed with `gcc -v`, and Make is installed with `make -v`.

At this point [the official documentation says](https://jekyllrb.com/docs/installation/#install-with-rubygems) to use `gem install jekyll`, but this fails with:

    ERROR:  While executing gem ... (Gem::FilePermissionError)
        You don't have write permissions for the /var/lib/gems/2.3.0 directory.

The solution seems to be changing the version of Ruby to 2.3.0, matching the version used by RubyGems. Verify this by running `gem env` and `which ruby` to see if they match. The *RUBY EXECUTABLE* directory should match the directory shown with `which ruby`. If not, install Ruby 2.3.0 using `rvm install ruby-2.3.0` and set it as the version used by Ruby Version Manager using `rvm use ruby-2.3.0`. Using `gem install jekyll` should now work correctly. Also use `gem install bundler` as this is apparently also required [despite not being listed among Jekyll's installation requirements](https://jekyllrb.com/docs/installation/#requirements). Some [Jekyll themes](https://jekyllrb.com/docs/themes/) may also require `sudo apt install cmake`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of comparing Ruby versions was introduced to me by [an answer on Ask Ubuntu by Gilles](https://askubuntu.com/questions/142720/cant-run-a-program-installed-through-gem-install/163151#163151).

[Jekyll]: https://jekyllrb.com/
