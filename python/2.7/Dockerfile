#
# NOTE: THIS DOCKERFILE IS GENERATED VIA "update.sh"
#
# PLEASE DO NOT EDIT IT DIRECTLY.
#

FROM python:2.7-alpine

# 安装Python库
RUN set -ex; \
	\
	pip install --upgrade pip; \
	\
	pip install mongo redis requests xlwt; \
	\
	mkdir /www; \
	\
	python --version; \
