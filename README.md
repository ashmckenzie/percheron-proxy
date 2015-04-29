# Percheron HAProxy + nginx Stack

This repo contains a complete HAProxy + nginx stack for use with [Percheron](https://github.com/ashmckenzie/percheron).

## Containers included

* base (just an image, used by all containers)
* front-lb - Load balancer that sees requests first (HAproxy)
* front-proxy (2) - Proxy off to App load balancers (nginx)
* app-lb (2) - Load balancer for app (HAproxy)
* app (2) - Servers 200 for any request (nginx)

## Dependancies

* [Percheron](https://github.com/ashmckenzie/percheron)
* [Boot2Docker v1.6.x+](https://docs.docker.com/installation)
* [Docker client](https://docs.docker.com/installation) (nice to have)

## Quickstart

Start boot2docker

````shell
boot2docker up && eval $(boot2docker shellinit) && export BOOT2DOCKER_IP=$(boot2docker ip)
```

Clone the percheron-proxy repo

```shell
git clone https://github.com/ashmckenzie/percheron-proxy
```

Run Percheron!

```shell
cd percheron-proxy && bundle install && bundle exec percheron start proxy
```
