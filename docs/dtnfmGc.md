# determining which files have the most [Git] commits

Ha! that's one of these things that is very easy, accidentally (?):

```
git rev-list --objects --all | awk '$2' | sort -k2 | uniq -cf1 | sort -rn | head
```

1. give me all objects from all revisions in all branches
2. ignore any results without a path
3. sort them by path
4. make them unique (ignoring the blob hash), prefix lines with duplication count
5. sort descending on duplication count
6. show topmost lines

Output similar to

```
1058 fffcba193374a85fd6a3490f800c6901218a950b src
 715 ffffe0f08798e95b66cc4ad4ff22cf10734d045e src/lib
 450 ffcfe596031a5985664e35937fff4ac9ff38dcca src/zfs-fuse
 367 ffc5d5340f95360fc9f7b739c5593dd3f92fced0 src/lib/libzpool
 202 ff92db000792044d45eec21c57a3cd21618631e7 src/lib/libsolkerncompat
 183 ff1a44edae3fd121ddd86864b589e5ab2f9ff99b src/lib/libzfscommon
 178 fec6b3a789e578983c2242b3aa5adf217cb8b887 src/lib/libzfs
 168 ffeefc9e81222d7c471bdb0911d8b98f23cff050 src/cmd
 167 fbd60bd3430765863648c52db7ceb3ffa15d5e50 src/lib/libzfscommon/include
 155 ff225f6b41f9557d683079c5f9276f497bcb06bd src/lib/libzfscommon/include/sys
```

You can take it from here.

## E.g. if you **wanted to see only file blobs**:

```
git rev-list --objects --all | awk '$2' | sort -k2 | uniq -cf1 | sort -rn |
    while read frequency sample path
    do 
       [ "blob" == "$(git cat-file -t $sample)" ] && echo -e "$frequency\t$path";
    done
```

**output**:

```
135 src/zfs-fuse/zfs_operations.c
84  src/zfs-fuse/zfs_ioctl.c
79  src/zfs-fuse/zfs_vnops.c
73  src/lib/libzfs/libzfs_dataset.c
67  src/lib/libzpool/spa.c
66  src/zfs-fuse/zfs_vfsops.c
62  src/cmd/zdb/zdb.c
62  CHANGES
60  src/cmd/ztest/ztest.c
60  src/lib/libzpool/arc.c
```

## You wanted to see only specifc range of revisions

You can have a ball with the `rev-list` part:

```
git rev-list --after=2011-01-01 --until='two weeks ago' \
     tag1...remote/hotfix ^master
```

Will use only revisions in the specified date range, that are in the symmetric set difference for `tag1` and `remote/hotfix` and are **not** in master

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Stack Overflow by sehe](https://stackoverflow.com/questions/5669621/git-find-out-which-files-have-had-the-most-commits/5670168#5670168) with changes made, including converting the original HTML to Markdown.

[Git]: https://git-scm.com/
