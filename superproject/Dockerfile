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
        # dvipsk-ja \
        texlive \
        sshpass \
        ghostscript \
    && rm -rf /var/lib/apt/lists/* \
    && apt clean -y
