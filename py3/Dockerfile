FROM python:3.8.5-alpine3.12
LABEL name=pylint version=py3 maintainer=Linedwell

RUN apk add --no-cache --virtual .build-deps \
    musl-dev=1.1.24-r9 \
    gcc=9.3.0-r2 \
    && pip install --no-cache-dir \
    pylint==2.6.0 \
    pylint_junit==0.2.0 \
    pylint-exit==1.2.0 \
    pylint-json2html==0.2.0 \
    && pip uninstall pip -y \
    && apk del .build-deps
