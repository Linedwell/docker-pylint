FROM python:3-alpine
MAINTAINER "Linedwell"

#RUN apk add --no-cache \
#    git \
#    openssh-client

RUN apk add --no-cache --virtual .build-deps \
    musl-dev \
    gcc \
    && pip install --no-cache-dir --pre pylint pylint-exit \ 
    && apk del .build-deps
