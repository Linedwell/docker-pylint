FROM python:2.7.17-alpine3.10
LABEL name=pylint version=py2 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.22-r3 \
    gcc=8.3.0-r0 \
    && pip install --no-cache-dir \
    pylint==1.9.4 \
    pylint-exit==1.0.0 \
    && pip uninstall pip -y \
    && apk del .build-deps
