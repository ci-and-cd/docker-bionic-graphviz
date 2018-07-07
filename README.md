# docker-bionic-graphviz

Graphviz on Ubuntu 18.04 (bionic) for multi-stage docker image build.

Dockerfile [ci-and-cd/docker-bionic-graphviz on Github](https://github.com/ci-and-cd/docker-bionic-graphviz)

[cirepo/bionic-graphviz on Docker Hub](https://hub.docker.com/r/cirepo/bionic-graphviz/)

## Use this image as a “stage” in multi-stage builds

```dockerfile

FROM ubuntu:18.04
COPY --from=cirepo/bionic-graphviz:latest-archive /data/root /

```
