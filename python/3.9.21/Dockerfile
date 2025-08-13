#
# NOTE: THIS DOCKERFILE IS GENERATED VIA "update.sh"
#
# PLEASE DO NOT EDIT IT DIRECTLY.
#

FROM python:3.9.21

# 安装Python库
RUN set -ex; \
	\
	pip install --upgrade pip; \
	\
	pip install langchain-community; \
	\
	pip install Flask; \
	\
	pip install openai; \
	\
	pip install sentence-transformers; \
	\
	pip install langchain-openai; \
	\
	pip install chromadb; \
	\
	mkdir /www; \
	\
	python --version; \