# Tabulify.com


## About



## How to run

* In Dev mode
```bash
docker run \
  --name site-com-tabulify \
  --rm \
  -p 8081:80 \
  --user 1000:1000 \
  -e DOKU_DOCKER_ENV=dev \
  -e DOKU_DOCKER_ACL_POLICY='public' \
  -e DOKU_DOCKER_ADMIN_NAME='admin' \
  -e DOKU_DOCKER_ADMIN_PASSWORD='welcome' \
  -v $PWD:/var/www/html \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```

## Note

### java-mono/website

This repository is also a submodule of `java-mono/website`
```
git submodule add
```
Make a [submodule](https://book.git-scm.com/book/en/v2/Git-Tools-Submodules)

