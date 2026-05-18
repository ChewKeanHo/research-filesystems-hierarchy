# `/dev`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all device nodes (special files).

The goal is simple: the operating system (OS) maps all the device nodes by
kernel into the filesystem for hardware-software interactions.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the OS distributor's documentation for the device nodes
definitions. For examples:

* Hard disk and USB storage devices can be repesented as:
  * `/dev/sdN` in `Linux` (e.g. `/dev/sda`)
* NVME storage devices can be represented as:
  * `/dev/nvmeMnN` in `Linux` (e.g. `/dev/nvme0n1`)
