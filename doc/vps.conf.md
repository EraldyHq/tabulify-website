# Server

## About

This is the configuration based on a VPS installation.

This is outdated as we have moved to a dokuwiki docker structure.

## Symlinks

```bash
FQDN=tabulify.com
ln -s /opt/www/git/${FQDN}/data/pages /opt/www/bytle/farmer-animals/${FQDN}/data/pages
ln -s /opt/www/git/${FQDN}/data/media /opt/www/bytle/farmer-animals/${FQDN}/data/media
#mkdir -p /opt/www/bytle/farmer-animals/${FQDN}/data/combo/theme/
#ln -s /opt/www/git/${FQDN}/theme /opt/www/bytle/farmer-animals/${FQDN}/data/combo/theme/combo
```

## Configuration

Installation if changed in the repo
```
mv /opt/www/bytle/farmer-animals/${FQDN}/conf/local.php-$(date -u +"%Y-%m-%d.%H:%M")
ln -s /opt/www/git/${FQDN}/conf/${FQDN}/local.php /opt/www/bytle/farmer-animals/${FQDN}/conf/local.php
```

After each update on the server. Configuration is overwritten. After every configuration change
```
cp /opt/www/bytle/farmer-animals/${FQDN}/conf/local.php  /opt/www/git/${FQDN}/conf/${FQDN}/local.php
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