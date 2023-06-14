FROM node:18-alpine 

RUN apk --no-cache add python3 py3-pip

RUN  pip3 install --upgrade pip \
  && pip3 install --no-cache-dir awscli

RUN npm install -g serverless

ENTRYPOINT [ "serverless" ]