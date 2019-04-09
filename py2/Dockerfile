FROM python:2.7.16-alpine3.9
LABEL name=pylint version=py2 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.20-r4 \
    gcc=8.3.0-r0 \
    && pip install --no-cache-dir \
    pylint==2.3.1 \
    pylint-exit==1.0.0 \
    && pip uninstall pip -y \
    && apk del .build-deps
