# `/root/.local/lib`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, library files (e.g. C object artifact files) personalized for
`root` account.

Generally, you **SHOULD** place `root` account own custom library files here.

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
/root/.local/lib/
  trademark/
    product/
      lib1.a
      lib1_freebsd-amd64.a
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/root/.local/lib/
  product/
    lib1.a
    lib1_freebsd-amd64.a
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
