FROM --platform=arm64 ubuntu:focal

ENV DOCKER_CLI_EXPERIMENTAL=enabled

RUN apt -y update && \
    apt -y install \
        apt-transport-https \
        ca-certificates \
        curl \
        make \
        awscli \
        software-properties-common && \
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
        gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
    echo "deb [arch=$(dpkg --print-architecture) \
        signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
        https://download.docker.com/linux/ubuntu \
        $(lsb_release -cs) stable" > /etc/apt/sources.list.d/docker.list && \
    apt -y update && \
    apt -y dist-upgrade && \
    apt remove -y docker-ce docker-ce-cli containerd.io docker-compose docker-compose-plugin && \
    apt install -y docker-ce docker-ce-cli containerd.io docker-compose docker-compose-plugin && \
    apt autoremove && \
    apt clean

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

# FROM gcr.io/cloud-builders/docker

# RUN apt install curl wget unzip bash -y

# RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip"

# RUN unzip awscliv2.zip

# RUN ./aws/install

# ENV DOCKER_CLI_EXPERIMENTAL=enabled

# ENTRYPOINT ["/usr/bin/docker"]