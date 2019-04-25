FROM ubuntu:xenial AS base
LABEL maintainer="damian.jarek93@gmail.com"

WORKDIR /root

RUN apt update && apt install -y \
        valgrind \
        lcov \
        software-properties-common \
        gdb \
        curl \
        libssl-dev


FROM base AS compilers
LABEL maintainer="damian.jarek93@gmail.com"

RUN apt-add-repository -y "ppa:ubuntu-toolchain-r/test" \
    && curl https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add - \
    && apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-8 main" \
    && apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-7 main" \
    && apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-6.0 main" \
    && apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-5.0 main" \
    && apt-add-repository ppa:git-core/ppa \
    && apt update \
    && apt install -y \
        clang-8 libc++-8-dev libc++abi-8-dev \
        clang-7 \
        clang-6.0 \
        clang-5.0 \
        clang \
        g++-8 \
        g++-7 \
        g++-6 \
        g++ \
        git \
    && apt purge -y --autoremove software-properties-common \
    && rm -rf /var/lib/apt/lists/* \
    && apt clean -y
