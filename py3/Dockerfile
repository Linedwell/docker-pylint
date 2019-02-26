FROM python:3.7.1-alpine3.8
LABEL name=pylint version=py3 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.19-r10 \
    gcc=6.4.0-r9 \
    && pip install --no-cache-dir pylint==2.1.1 pylint-exit==1.0.0 \
    && pip uninstall pip \
    && apk del .build-deps
