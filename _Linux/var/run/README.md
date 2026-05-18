# `/var/run`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) files containing information
about the OS since it was booted.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.

In certain Linux-based OSes such as Debian Linux, this directory is symlinked
to `/run` directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to your OS's documentations for device nodes definitions. In
any case, just like the OS takes over this entire directory.
