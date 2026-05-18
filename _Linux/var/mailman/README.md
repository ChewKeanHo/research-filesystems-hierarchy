# `/var/mail`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `mailman` data files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users.

This directory is **ENTIRELY OPTIONAL** depending on the OS' uses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `mailman` manual.
