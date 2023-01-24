FROM ubuntu:12.04

LABEL author="Muh Aqila Naufal Hakim" maintainer="muhaqilanaufalhakim@gmail.com"

LABEL org.opencontainers.image.source="https://github.com/manh21/yolks"
LABEL org.opencontainers.image.licenses=MIT

ENV DEBIAN_FRONTEND=noninteractive

## change repo links
RUN sed -i -e 's/archive.ubuntu.com\|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list

## update base packages
RUN apt-get update

## install dependencies
RUN apt-get install -y curl unzip mumble-server python-zeroc-ice zeroc-ice \
    libicu48 libprotobuf7 libcap2 libiceutil34 libzeroc-ice34 libqt4-dbus libqt4-sql libqt4-sql-sqlite libqt4-network libicu48