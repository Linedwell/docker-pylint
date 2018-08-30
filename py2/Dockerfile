FROM python:2-alpine
MAINTAINER "Linedwell"

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.18-r3 \
    gcc=6.4.0-r5 \
    && pip install --no-cache-dir pylint=1.9.2 pylint-exit=0.8.3 \ 
    && apk del .build-deps
