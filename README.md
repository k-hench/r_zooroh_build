# README for `r_zooroh`

Github repository for the [podman](https://podman.io/) container [`r_zooroh`](https://hub.docker.com/repository/docker/khench/r_zooroh).

## Documentation of the initial setup

Originally, the `r_zooroh` container was build using [buildah](https://buildah.io/), from the accompanying `Containerfile`:

```sh
buildah bud -t r_zooroh
```

To make the container publicly available, it is pushed to [dockerhub](https://hub.docker.com/r/khench/r_zooroh) using [skopeo](https://github.com/containers/skopeo) and [podman](https://podman.io/):

```sh
skopeo login -u khench docker.io
podman push localhost/r_zooroh docker.io/khench/r_zooroh:v0.2
```

## Accessing the container

The bundled software can be accessed directly from [dockerhub](https://hub.docker.com/r/khench/r_zooroh) with `podman` (or `docker`, or `singularity`):

```sh
podman run docker.io/khench/r_zooroh:v0.1 which R
```
