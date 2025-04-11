# Tabulify.com


## About

This Git repo contains [tabulify.com](https://tabulify.com) written with the [Combo Site Technology](https://combostrap.com/admin/combostrap-website-yfi22ewn)


## How

### How to Run

```bash
docker run \
  --name site-com-tabulify \
  --rm \
  -p 8081:80 \
  -e DOKU_DOCKER_GIT_SITE='https://github.com/EraldyHq/tabulify-website' \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```

* With SSH
```bash
docker run \
  --name site-com-tabulify \
  --rm \
  -p 8081:80 \
  -e DOKU_DOCKER_GIT_SITE='git@github.com:EraldyHq/tabulify-website.git' \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```



## Contribute


See [contribute](contribute/contribute.md)
