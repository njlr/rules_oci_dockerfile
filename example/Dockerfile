FROM mcr.microsoft.com/dotnet/runtime-deps:6.0.10-bullseye-slim-amd64@sha256:24554fadd483d8305974ded44bb1dbe4916e2f02500b9e2d78e7beb557cfebd0

ARG DEBIAN_FRONTEND=noninteractive

ENV LC_ALL=C.UTF-8 \
    LANG=C.UTF-8 \
    LANGUAGE=C.UTF-8

RUN apt-get -y update \
    && apt-get -y install git \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
