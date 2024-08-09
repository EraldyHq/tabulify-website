# Tabulify.com


## About



## How to run

* In Dev mode
```bash
docker run --name dokuwiki \
  --rm \
  -p 8080:80 \
  -e DOKU_DOCKER_ENV=dev \
  -e DOKU_DOCKER_GIT=https://github.com/Tabulify/tabulify.com \
  -v 'c:\temp\dokuwiki':/var/www/html \
  ghcr.io/combostrap/dokuwiki:php8.3-v1
```

## Note

### java-mono/website

This repository is also a submodule of `java-mono/website`
```
git submodule add
```
Make a [submodule](https://book.git-scm.com/book/en/v2/Git-Tools-Submodules)

