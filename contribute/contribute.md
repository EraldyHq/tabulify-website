# Contribution

## Steps

### Clone

> [!IMPORTANT]
> If you are not member of the Eraldy Organisation, you need to create and clone a fork.

* Only this repository
```bash
# without the tabulify code
git clone git@github.com:EraldyHq/tabulify-website.git
cd tabulify-website
```
* With the tabulify repository (as it is a [submodules](https://github.com/EraldyHq/tabulify/.gitmodules))
```bash
git clone --recurse-submodules https://github.com/EraldyHq/tabulify
cd tabulify-cli/src/main/tabulify.com
```


### Run


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
  -e DOKU_DOCKER_BASE_URL='http://tabulify.dev' \
  -v $PWD:/var/www/html \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```

