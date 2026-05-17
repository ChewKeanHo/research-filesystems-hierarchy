# `/root/.cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing cache files from `root`
account's programs and applications. Most UNIX and UNIX-like operating system
(OS)s create this directory as it is. Otherwise, modern OSes symlinked it to the
`/root/.local/var/cache` directory, a `.local` common directory for consistency
with the filesystem hierarchy standards.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Programs that used this directory **SHOULD** remove the cache files to avoid
data poisoning or corruption after use.

To symlink this directory to `/root/.local/var/cache` manually, simply execute
the following command:

```
# cd "/root"
$ mkdir -p "./.local/var/cache"
$ if [ -d "./.cache" ]; then do mv "./.cache/*" "./.local/var/cache/."; done
$ rm -rf "./.cache" &> /dev/null
$ sync .
$ ln -s "./.cache" "./.local/var/cache"
```
