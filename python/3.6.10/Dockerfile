#
# NOTE: THIS DOCKERFILE IS GENERATED VIA "update.sh"
#
# PLEASE DO NOT EDIT IT DIRECTLY.
#

FROM python:3.6.10

# 安装Python库
RUN set -ex; \
	\
	pip install --upgrade pip; \
	\
	pip install mongo mysql redis requests mysqlclient xlwt kafka; \
	\
	pip install -i https://pypi.tuna.tsinghua.edu.cn/simple apache-airflow; \
	\
	mkdir /www; \
	\
	python --version; \
