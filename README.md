# Percheron HAProxy + nginx Stack

This repo contains a complete HAProxy + nginx stack for use with [Percheron](https://github.com/ashmckenzie/percheron).

## Containers included

* base (just an image, used by all containers)
* haproxy
* proxy (2)
* app (2)

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
