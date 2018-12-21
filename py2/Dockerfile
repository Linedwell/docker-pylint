FROM python:2.7.15-alpine3.8
LABEL name=pylint version=py2 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.19-r10 \
    gcc=6.4.0-r9 \
    && pip install --no-cache-dir pylint==1.9.2 pylint-exit==1.0.0 \ 
    && apk del .build-deps
