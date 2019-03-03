FROM ubuntu:xenial
LABEL maintainer="damian.jarek93@gmail.com"

WORKDIR /root

RUN apt update && apt install -y \
        p7zip-full  \
        docutils-common \
        docutils-doc \
        docbook \
        docbook-xml \
        docbook-xsl \
        dvipsk-ja \
        xsltproc \
        doxygen \
        openssh-client \
        git \
        texlive \
        sshpass \
        ghostscript \
        unzip \
        wget \
        python-pip \
        ruby \
    && rm -rf /var/lib/apt/lists/* \
    && apt clean -y
