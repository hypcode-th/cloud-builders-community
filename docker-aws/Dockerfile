# FROM python:3-alpine
# RUN apk add --update \
#     groff \
#     less  \
#     curl \
#     wget \
#     git \
#     docker \
#     openrc \
#     bash \
#     ca-certificates \
#   && pip install --no-cache-dir awscli \
#   && rm -rf /var/cache/apk/* ~/.cache/pip
# ENV PAGER=less

# ENTRYPOINT [ "bash" ]

FROM gcr.io/cloud-builders/docker

RUN apt install curl wget unzip bash -y

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

RUN unzip awscliv2.zip

RUN ./aws/install

ENV DOCKER_CLI_EXPERIMENTAL=enabled

ENTRYPOINT ["/usr/bin/docker"]