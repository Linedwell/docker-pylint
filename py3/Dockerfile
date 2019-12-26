FROM python:3.8.1-alpine3.10
LABEL name=pylint version=py3 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.22-r3 \
    gcc=8.3.0-r0 \
    && pip install --no-cache-dir \
    pylint==2.3.1 \
    pylint-exit==1.0.0 \
    pylint-json2html==0.1.0 \
    && pip uninstall pip -y \
    && apk del .build-deps
