---
title: Create a file of any size
category: Tip
date: '2021-03-19 20:07:00 +7'
topics: macOS
---

Sometimes we need big files for testing purposes, without any concern for the files' content. For example, when testing uploads, downloads & responding to changes in network performance, we are likely to want files of various sizes.

macOS comes with a helpful utility command to create a file of any size over 512 bytes called `mkfile`:

```shell
$ mkfile FILE_SIZE FILE_NAME
```

In the `FILE_SIZE` option, we can optionally use a suffixes to note the unit of the value  `b` - bytes (the deafult), `k` - kilobytes, `m` - megabytes or `g` - gigabytes.

For example, the following command produces an empty two gigabyte file named `big-file.ext`:

```shell
$ mkfile 2g big-file.ext
```

Note the following multiplication factors are applied to the `FILE_SIZE` value:

|Unit|Factor|Examples|
|-|-|-|
|`b`|512|For 512 bytes: `1b`, for 1kb (1024 bytes): `2b`|
|`k`|1024|For 1kb (1024 bytes): `1k`, for 1mb (1,048,576 bytes): `1024k`|
|`m`|1048576|For 1mb (1,048,576 bytes): `1m`, for 1gb (1,073,741,824 bytes): `1024m`|
|`g`|1073741824|For 1mb (1,073,741,824 bytes): `1g`, for 2gb (2,147,483,648 bytes): `1g`|

See the man page for `mkfile` for more information.

```shell
$ man mkfile
```
### See also

-   [Create a big file on Linux](/create-a-big-file-on-linux.html)
