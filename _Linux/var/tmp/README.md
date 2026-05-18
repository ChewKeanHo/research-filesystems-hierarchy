# `/var/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's temporary files and directory.
Unlike `/tmp` base directory, this temporary directory **get persisted** across
reboot (without deletion) enabling post booting forensic analytics use.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and after use to
avoid post-use blaming or corrupted data usage.

In majority of Linux-based OSes, this directory is replaced by `/tmp` directory.
For some like Red Hat Linux and Fedora, this directory is a direct replacement
of `/tmp` directory and symlinked to `/usr/tmp` temporary directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/tmp/
  trademark/
    product/
    ...

OR

/var/tmp/
  product/
    ...
```
