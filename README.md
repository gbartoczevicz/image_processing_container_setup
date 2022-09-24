# Image Processing Container Setup

This repository aims for creating a setup with Python in a Docker container with
some stuff related with image processing and machine learning.

## Requirements

- VSCode
- Docker

## How to

After installing the VSCode editor and Docker you will need to install the
**Remote - Containers** extension for VSCode, and then just follow the extension
instructions if needed.

When opening this project, you'll open this folder remotely with the extension
and then the extension will create a Docker container following the
`.devcontainer`'s `Dockerfile` and `devcontainer.json` files and then will
connect to the remote itself (the container running).

If needed you can install some pip dependencies listed on requirements.txt by
adding a new one on it. When building the container the Dockerfile will run
`pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt`
to install the dependencies. Follow the Dockerfile definition to change it if
needed.

Every time that a dependency is added to the file remind to rebuild the
container, and keep in mind that if rebuilding the container without cache will
increase the load time during the dependencies installation.

## Useful links

- Developing inside a Container: https://code.visualstudio.com/docs/remote/containers
