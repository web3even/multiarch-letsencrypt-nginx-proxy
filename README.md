## nginx-proxy with letsencrypt-nginx-proxy-companion on armhf and arm64

This repo provide a simplified way to run up to date [nginx-proxy](https://github.com/jwilder/nginx-proxy) stack with [Let's Encrypt support](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion) on non `amd64` architectures.

It requires [docker-compose](https://docs.docker.com/compose/install/#install-compose) to run.

### Usage:

1. `git clone https://github.com/buchdag/multiarch-letsencrypt-nginx-proxy`

2. `cd multiarch-letsencrypt-nginx-proxy`

3. `docker-compose up -d`

Certificate issuance was sucessfully tested on [Scaleway](https://www.scaleway.com/) `C1` and `ARM64-2GB` servers.

The two multi-stage Dockerfiles will produce a build container that won't be automatically cleaned afterwards. You can remove it with `docker image prune --filter label=stage=intermediate`.
