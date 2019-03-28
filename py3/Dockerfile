FROM python:3.7.2-alpine3.9
LABEL name=pylint version=py3 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.20-r4 \
    gcc=8.2.0-r2 \
    && pip install --no-cache-dir \
    pylint==2.1.1 \
    pylint-exit==1.0.0 \
    && pip uninstall pip -y \
    && apk del .build-deps
