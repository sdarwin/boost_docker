FROM ubuntu:xenial
LABEL maintainer="damian.jarek93@gmail.com"

WORKDIR /root

RUN apt update && apt install -y \
        p7zip-full  \
        curl \
        docutils-common \
        docutils-doc \
        docbook \
        docbook-xml \
        docbook-xsl \
        dvipsk-ja \
        xsltproc \
        openssh-client \
        git \
        graphviz \
        texlive \
        sshpass \
        ghostscript \
        unzip \
        wget \
        python-pip \
        ruby \
        python-docutils \
        libsaxonhe-java \
        cmake \
        bison \
        flex \
        texlive-latex-extra \
    && git clone -b 'Release_1_8_15' --depth 1 https://github.com/doxygen/doxygen.git \
    && cd doxygen \
    && cmake -H. -Bbuild -DCMAKE_BUILD_TYPE=Release \
    && cd build \
    && make install \
    && cd && rm -rf doxygen* \
    && rm -rf /var/lib/apt/lists/* \
    && apt clean -y
