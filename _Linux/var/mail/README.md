# `/var/mail`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) user email files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users.

This directory is **ENTIRELY OPTIONAL** depending on the OS' uses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `mail`** as it represent the entire mail
directory.

The file extension can be anything and nothing.

It is a practice to house the files using `trademark` and `product` naming
convention pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/mail/
  trademark_product
  ...

OR

/var/mail/
  product
  ...
```
