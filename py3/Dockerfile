FROM python:3-alpine
LABEL name=pylint version=py3 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.20-r0 \
    gcc=6.4.0-r8 \
    && pip install --no-cache-dir pylint==1.7.4-r1 pylint-exit==1.0.0 \
    && apk del .build-deps
