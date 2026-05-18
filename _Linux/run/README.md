# `/run`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all operating system's (OS) runtime system
files containing information about the OS since it was booted.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.

In certain Linux-based OSes such as Debian Linux, this directory is symbolically
linked from various locations (e.g. `/var/run`) for reducing number of tmpfs
file systems.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the OS distributor's documentation for the nodes
definitions.
