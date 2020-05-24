# UPMEM in Docker

## Pull from Docker Hub

Docker Hub images are built from the code in this repository. Alternatively [build an image from source](#Build).

```shell
docker pull johnramsden/upmem
```

## Build

If you would prefer to build your own image instead of using a pre-built one, clone this repository and build from source.

```shell
docker build . -t upmem
```

## Usage

Place code to mount into container on local filesystem, `~/upmem` used in below example.

Run container, mounting a directory into the container:

```shell
docker run --interactive --tty \
    --volume="${PWD}:/home/upmem/upmem" upmem
```

## Multiple Terminals

To open up multiple terminals use `tmux` inside the container.

or `docker exec` into an already running container.

```shell
docker exec --interactive --tty <id> /bin/bash
```

---

References:

* https://sdk.upmem.com/
* https://sdk.upmem.com/2020.2.1/01_Install.html
* https://bitworks.software/en/2017-07-24-docker-ptrace-attach.html

Licenced MIT
