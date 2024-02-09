# Tabulify.com


## Submodule

This repository is a submodule of `java-mono/db/website`

```
git submodule add
```

## How to run

### The stick

See the stick.md file in the combo dev repo.

```cmd
C:\DokuWikiStick\run.cmd
```

### Dev Farm Apache Server

Stop the Apache Service

Then

* If Directory (first time) where `nico.lan` should be replaced with the name of the host
```bash
rm /S D:\dokuwiki-animals\tabulify.nico.lan\conf\local.php
rmdir /S D:\dokuwiki-animals\tabulify.nico.lan\data\media
rmdir /S D:\dokuwiki-animals\tabulify.nico.lan\data\pages
```

* If symlink

```bash
rm D:\dokuwiki-animals\tabulify.nico.lan\conf\interwiki.local.conf
rm D:\dokuwiki-animals\tabulify.nico.lan\conf\local.php
rm D:\dokuwiki-animals\tabulify.nico.lan\data\media
rm D:\dokuwiki-animals\tabulify.nico.lan\data\pages
```

* Then create File Symlink
```bash
mklink "D:\dokuwiki-animals\tabulify.nico.lan\conf\interwiki.local.conf" "D:\code\java-mono\db-website\src\doc\tabulify.com\conf\interwiki.local.conf"
mklink "D:\dokuwiki-animals\tabulify.nico.lan\conf\local.php" "D:\code\java-mono\db-website\src\doc\tabulify.com\conf\local.php"
```
* Then create Directory Symlink
```bash
mklink /D "D:\dokuwiki-animals\tabulify.nico.lan\data\media"  "D:\code\java-mono\db-website\src\doc\tabulify.com\media"
mklink /D "D:\dokuwiki-animals\tabulify.nico.lan\data\pages"  "D:\code\java-mono\db-website\src\doc\tabulify.com\pages"
```

## Others

Make a [submodule](https://book.git-scm.com/book/en/v2/Git-Tools-Submodules)
