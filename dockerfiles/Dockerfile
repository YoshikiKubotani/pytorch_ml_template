#
ARG NVIDIA_CONTAINER_IMAGE_VERSION=21.03

# base image
FROM nvcr.io/nvidia/pytorch:${NVIDIA_CONTAINER_IMAGE_VERSION}-py3

LABEL maintainer "Yoshiki Kubotani <yoshikikubotani.lab@gmail.com>"

RUN apt update && DEBIAN_FRONTEND noninteractive apt install --no-install-recommends -y \
    htop \
    && rm -rf /var/lib/apt/lists/*

# poetry
RUN pip3 --proxy=${HTTP_PROXY} --no-cache-dir install poetry