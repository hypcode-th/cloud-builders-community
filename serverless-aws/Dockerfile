FROM node:18-alpine 
RUN apk add --update --no-cache bash python3 py3-pip docker openrc

RUN  pip3 install --upgrade pip --break-system-packages \
  && pip3 install --no-cache-dir awscli --break-system-packages

RUN npm install -g serverless

ENTRYPOINT [ "bash" ]