FROM mcr.microsoft.com/cbl-mariner/base/core:2.0

RUN tdnf install -y \
        sudo \
        tar \
        util-linux

RUN touch /tmp/install.tar.gz && \
    tar -cpzf /tmp/install.tar.gz \
        --exclude=/install.tar.gz \
        --exclude=/mnt/* \
        --exclude=/var/cache/* \
        --exclude=/tmp/* \
        --exclude=.dockerenv \
        --one-file-system /
