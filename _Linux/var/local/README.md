# `/var/local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) localized programs and
applications' (programs from `/usr/local`) persistent data. Due to its
processing nature, one **MUST** carefully work here to prevent any data
poisoning or losses.

All files here are available to all users.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/local/
  trademark/
    product/
      data.save
      profile1.jpg
      transient.json
      ...

# OR

/var/local/
  product/
    data.save
    profile1.jpg
    transient.json
    ...
```
