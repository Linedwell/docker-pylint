FROM python:2-alpine
LABEL name=pylint version=py2 maintaine=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.19-r10 \
    gcc=6.4.0-r8 \
    && pip install --no-cache-dir pylint==1.9.2 pylint-exit==1.0.0 \ 
    && apk del .build-deps
