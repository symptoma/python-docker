# python-docker

Python Docker Image with Docker Client included. Available with Python 3.11.

Published on the Docker Hub: https://hub.docker.com/r/symptoma/python-docker

## Multi Architecture Docker Build

Prepare the buildx context and use it:

BUILDER_NAME=$(docker buildx create) && docker buildx use $BUILDER_NAME

Then build for multiple platforms:

docker buildx build --push --platform linux/arm64,linux/amd64 --tag symptoma/python-docker:3.11 .