# `/root/.local/share`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific architecture independent data files (e.g. PDF files, SVG vector
files, etc) personalized for `root` account.

All files here are available only to the `root` account.

Generally, you **SHOULD** place `root` account own custom architecture
independent data files here.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/root/.local/share/
  trademark/
    product/
      docs/
        README.pdf
        Terms-of-Service.pdf
        ...
      licenses/
        LICENSE.pdf
        LICENSE.txt
        LICENSE.html
        ...
      ...

# OR

/root/.local/share/
  product/
    docs/
      README.pdf
      Terms-of-Service.pdf
      ...
    licenses/
      LICENSE.pdf
      LICENSE.txt
      LICENSE.html
      ...
    ...
```
