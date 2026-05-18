# `/proc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all process nodes (special files). This
directory appears only when absolutely needed (e.g. FreeBSD enabling Linux
inter-compatibility layer which requires `/proc` to exist). On Linux, it is
always exist for backward compatibilities purposes.

The goal is simple: allow OS process filesystems (e.g. `procfs`) to map
every process files into filesystems for use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the OS distributor's documentation for the device nodes
definitions.
