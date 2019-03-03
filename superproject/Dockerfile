FROM debian:buster
LABEL maintainer="damian.jarek93@gmail.com"

WORKDIR /root

RUN apt update && apt install -y \
        p7zip-full  \
        docutils-common \
        docutils-doc \
        docbook \
        docbook-xml \
        docbook-xsl \
        xsltproc \
        doxygen \
        openssh-client \
        git \
        texlive \
        sshpass \
        ghostscript \
        unzip \
        wget \
    && rm -rf /var/lib/apt/lists/* \
    && apt clean -y
