ARG IMAGE=ghcr.io/vipm-io/actions-runner-labview-2024-linux
ARG TAG=main
FROM ${IMAGE}:${TAG}

RUN \
    chmod -R ugo+rw /usr/local/JKI && \
    chmod -R ugo+rw /etc/JKI && \
    chmod ugo+x /usr/local/JKI/VIPM/vipm

# RUN \
#     apt-get update -y && \
#     apt-get install -y sqlite3

USER labview
ENV USER=labview
