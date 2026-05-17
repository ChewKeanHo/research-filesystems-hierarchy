# `/root/.local/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific transient data files (e.g. state files, saved games files, web
server files, log files, etc) personalized for `root` account.

Generally, you **SHOULD** place `root` account custom transient data files here.

All files here are available only to the `root` account.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/root/.local/var/
  trademark/
    product/
      log/
        access.log
        info.log
        ...
      cache/
        icons/
          banner_1200x1200.svg
          ...
      ...

# OR

/root/.local/var/
  product/
    log/
      access.log
      info.log
      ...
    cache/
      icons/
        banner_1200x1200.svg
        ...
    ...
```
