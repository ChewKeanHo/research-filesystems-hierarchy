# `/usr/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses the operating system's (OS) `/usr`'s temporary files and
directory.

On majority of UNIX-like OSes, this directory is unused. However, for some like
Red Hat Linux and Fedora, this directory is symlinked from `/tmp` directory and
itself is symlinked to `/var/tmp` directory ( `/tmp -> /usr/tmp -> /var/tmp`).
In short, if this directory is used, then `/tmp` should not be available.

On many OSes design, this directory gets cleared and cleaned on boot up.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and after use to
avoid post-use blaming or corrupted data usage.

The details are the same as [/tmp](/_Linux/tmp).
