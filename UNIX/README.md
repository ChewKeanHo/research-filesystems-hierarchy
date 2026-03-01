# UNIX Filesystem Hierarchy Standard

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is UNIX specific Filesystem Hierarchy Standard (FHS) covering all
compatible operating systems (OS) such as but not limited to:

* [`Berkeley Software Distribution` (BSD)](/_FreeBSD)
* [`GNU's Not Unix!` (GNU) + Linux](/_Linux)

For OS specific filesystems, please review their specific filesystems.




# Understanding The 4 Stages of Functionalities Extensions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

UNIX operating systems generally go through 4 stages of functionalities
extensions:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. This only uses tools from the Root (`/`) directory
   excluding any system directories mounting (e.g. `/usr`). The goal varies
   depending on the system's holistic design ranging from operating entirely
   in a resources limited environment (e.g. as OpenWRT router firmware),
   performing operating systems self-rescue, or extending its functionality
   to the next level.
2. **Full Catalogue** - focuses on extending the OS' functionalities upto its
   full potentials. This involves mounting the OS system directories (`/usr`).
   The goal here is to extend the OS' capabilities upto to the OS distributor's
   warranted functionalities with their supplied software packages.
3. **Complete** - focuses on extending the OS' functionalities further
   with user introduced system-wide functionalities. This involves mounting
   the OS' localized system directories (`/usr/local`). The goal here is to
   completely make the OS fully functional with localized functionalities
   (e.g. custom downloaded software packages setup by the user for all users).
   At this point, the OS' functionalities are marked as completed.
4. **Personalized** - focuses on extending the OS' functionalities with
   user-specific system directories (`/home/USERNAME/.local`). This stage can
   change from time-to-time across different users as it based on the
   user-only configurations.




## The Root

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The root directory is the very foundational and critical directory
represented by `/` in UNIX OS. When root combines with [Common](/Common)
filesystem hierarchy, you get a list of basic functional directories such as:

```
/bin       - OS critical user utilities programs.
/etc       - OS critical configuration files and scripts.
/lib       - OS critical libraries used by `/bin` and `/sbin` programs.
/sbin      - OS critical system administration (sysadmins) programs.
/tmp       - OS temporary work files.
```

The root directory also has other system directories that provides
various system roles:

```
/boot      - OS critical bootloading component.
/dev       - OS mapped IO device nodes for hardware interactions.
/home      - OS users' home directories (optional).
/media     - OS mounted removable media like CDs, floppy disks, and portable
             disks.
/mnt       - temporary mountpoint for sysadmins and root users to troubleshoot
             mountable nodes and devices.
/root      - OS root account's home directory (optional).
/usr       - OS UNIX Systems Resources for extended functionalities.
/var       - OS variable data directory like log, data, and spool files.
```

Then, the specific UNIX distribution (e.g. `FreeBSD`, `Debian`, etc) can
specify its specific directories such as but not limited to:

```
FreeBSD
-------
/compat    - Files supporting binary compatibilities with other operating
             systems like linux (`/compat/linux`).
/entropy   - Provides initial state to random number generator (RNG).
/net       - Automounted Network Area Storage (NAS) share mounting.
/rescue    - Statically linked programs for emergency recovery.


GNU+Linux
---------
/proc      - OS process files (optional).
/sys       - OS sysfs (optional). On Linux it's kernel info. On BSD, it's
             a symlinked to '/usr/src/sys'.
```




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to boot the OS critical component
up and running with minimum resources and be functionally operational.
This is known as `Single User` operating mode in FreeBSD or `Emergency Mode`
in many Linux-based OSes.

There are 2 possibilities:

* user use the operating system as it is (commonly seen in bare-metal
  embedded deployment like OpenWRT project); OR
* operating system expands to its full potentials by mount and load
  the `/usr` directory (common computing deployment).

You can explore each root layer's base directories in details. Once
done, head over to [`/usr`](/UNIX/usr) directory which is the second
layer for functionalities' expansions.
