FROM python:2-alpine
MAINTAINER "Linedwell"

RUN apk add --no-cache --virtual .build-deps \
    musl-dev \
    gcc \
    && pip install --no-cache-dir pylint pylint-exit \ 
    && apk del .build-deps
