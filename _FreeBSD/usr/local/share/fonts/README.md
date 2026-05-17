# `/usr/local/share/fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing user's system-wide, custom supplied,
non-critical, font files to extend the operating system (OS)'s functionalities
from *Full Catalogue* stage to *Complete* stage. This means it can operate in
both `Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities to its complete form by isolating
OS distributor's packages away from user's system-wide OS customizations. These
customizations, in theory, only specific to this machine instance.

All files here are available to all users.

Generally, you **SHOULD** place your own system-wide custom font files here.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/local/share/fonts/
  trademark/
    product1/
      font1.tff
      LICENSE.txt
      ...
    product2/
      font2.tff
      LICENSE.txt
      ...
    ...

# OR

/usr/local/share/fonts/
  product1/
    font1.tff
    LICENSE.txt
    ...
  product2/
    font2.tff
    LICENSE.txt
    ...
  ...
```
