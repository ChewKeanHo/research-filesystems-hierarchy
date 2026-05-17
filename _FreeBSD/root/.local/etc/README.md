# `/root/.local/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, configuration files personalized for `root` account only.

Generally, you **SHOULD** place `root` account's custom configuration files
here.

All files here are available only to the `root` account.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

The use of `.d` configuration directory strategy also reduces the configuration
complexities and making maintainability easier by just updating 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples:

```
/root/.local/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/root/.local/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
