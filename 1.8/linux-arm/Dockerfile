FROM golang:1.8

RUN echo "deb http://emdebian.org/tools/debian/ jessie main" >> /etc/apt/sources.list && \
    dpkg --add-architecture armhf && \
    curl http://emdebian.org/tools/debian/emdebian-toolchain-archive.key | apt-key add -

RUN apt-get update && \
    apt-get install -y crossbuild-essential-armhf && \
    rm -rf /var/lib/apt/lists/*

ENV CC arm-linux-gnueabihf-gcc
ENV CXX arm-linux-gnueabihf-g++

ENV CGO_ENABLED 1
ENV GOOS linux
ENV GOARCH arm
