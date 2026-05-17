# `/rescue`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all the critical programs, applications,
configuration files, libraries, and data files for the operating system (OS) to
perform its own self-rescue.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform OS self-rescue. All programs and applications here
are available to root account users operating `Single User` mode only.

Generally, you **SHOULD ONLY** place programs that are very critical at early
booting stage without conflicting with existing POSIX compliant programs.
