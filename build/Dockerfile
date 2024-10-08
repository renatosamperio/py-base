ARG REGISTER=docker.io
ARG VERSION=3.9.20
ARG SUFFIX=-bullseye

FROM ${REGISTER}/python:${VERSION}${SUFFIX}

RUN apt-get update && \
    apt-get -y install \
        build-essential \
        curl \
        git \
        wget

WORKDIR /opt/magnetter
COPY ./src/requirements.txt /opt/observer
RUN pip install -r src/requirements.txt

WORKDIR /var/tmp/src

