[![Build Status](https://gitlab.com/linedwell/docker-pylint/badges/master/build.svg)](https://gitlab.com/linedwell/docker-pylint)

# docker-pylint
Minimal docker images for linting Python files in CI based on Alpine Linux.

This container can be pulled with:
```bash
docker pull linedwell/pylint
```
# Tags
| Tag Name | Dockerfile  | Compressed Size |
|---|---|---|
| py2 | [py2/Dockerfile](//github.com/Linedwell/docker-pylint/blob/master/py2/Dockerfile) | Size: 27 MB |
| py3 | [py3/Dockerfile](//github.com/Linedwell/docker-pylint/blob/master/py2/Dockerfile) | Size: 39 MB |

# Content
This container is designed for running python lint checks on GitLab CI and similars. The following packages are installed:
* python 2.7.16 (for py2) or python 3.7.4 (for py3)
* pylint
* pylint-exit

# Usage
## Python Linting
```bash
docker run --rm -v $(pwd):/code -w "/code" linedwell/pylint:py2 \
  pylint  --output-format=colorized --reports=y \
  path/to/python/files
```
As pylint uses exit code to report analysis results (such as refactoring advices) you can first redirect your pylint exit to pylint-exit in order to have 0 as exit code if no fatal error has been found:

```bash
docker run --rm -v $(pwd):/code -w "/code" linedwell/pylint:py2 \
  pylint  --output-format=colorized --reports=y \
  path/to/python/files || pylint-exit $?
```
