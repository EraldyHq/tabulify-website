# Tabulify.com


## Submodule

This repository is a submodule of `bytle-mono/db/website`

```
git submodule add
```

## How to run

### The stick

See the stick.md file in the combo dev repo.

```cmd
C:\DokuWikiStick\run.cmd
```

### Dev Apache Server

Stop the Apache Service

Then

* If Directory (first time)
```bash
rm /S d:\dokuwiki\conf\local.php
rmdir /S d:\dokuwiki\data\media
rmdir /S d:\dokuwiki\data\pages
```

* If symlink

```bash
rm d:\dokuwiki\conf\local.php
rm d:\dokuwiki\data\media
rm d:\dokuwiki\data\pages
```

* Then Symlink
```bash
mklink /D "d:\dokuwiki\conf\local.php"  "D:\code\bytle-mono\db-website\src\doc\conf\local.php"
mklink /D "d:\dokuwiki\data\media"  "D:\code\bytle-mono\db-website\src\doc\media"
mklink /D "d:\dokuwiki\data\pages"  "D:\code\bytle-mono\db-website\src\doc\pages"
```

## Others

Make a [submodule](https://book.git-scm.com/book/en/v2/Git-Tools-Submodules)

