FROM python:3-alpine
RUN apk add --update \
    groff \
    less  \
    docker \
    openrc \
    bash \
  && pip install --no-cache-dir awscli \
  && rm -rf /var/cache/apk/* ~/.cache/pip
ENV PAGER=less

ENTRYPOINT [ "bash" ]