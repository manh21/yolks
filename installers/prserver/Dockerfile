FROM debian:bullseye-slim

LABEL author="Muh Aqila Naufal Hakim" maintainer="muhaqilanaufalhakim@gmail.com"

LABEL org.opencontainers.image.source="https://github.com/manh21/yolks"
LABEL org.opencontainers.image.licenses="MIT"

ENV DEBIAN_FRONTEND=noninteractive

RUN dpkg --add-architecture i386 \
    && apt update \
    && apt upgrade -y \
    && apt -y --no-install-recommends install ca-certificates curl lib32gcc-s1 libsdl2-2.0-0:i386 git unzip zip tar jq