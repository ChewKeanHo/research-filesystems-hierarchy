# `/root/.local/share/doc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific document files (e.g. man pages) personalized for `root` account.

Generally, you **SHOULD** place `root` account own custom document files here.

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
/root/.local/share/doc/
  trademark/
    product1/
      program.pdf
      program.txt
      program.1
      ...
    product2/
      program.pdf
      program.txt
      program.1
      ...
    ...

# OR

/root/.local/share/doc/
  product1/
    program.pdf
    program.txt
    program.1
    ...
  product2/
    program.pdf
    program.txt
    program.1
    ...
  ...
```
