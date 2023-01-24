FROM debian:bullseye-slim

LABEL author="Muh Aqila Naufal Hakim" maintainer="muhaqilanaufalhakim@gmail.com"

LABEL org.opencontainers.image.source="https://github.com/manh21/yolks"
LABEL org.opencontainers.image.licenses=MIT

ENV DEBIAN_FRONTEND=noninteractive

# add container user
RUN useradd -m -d /home/container -s /bin/bash container

# update base packages
RUN apt update

# install dependencies
RUN apt install -y gcc g++ libgcc1 libc++-dev gdb libc6 git wget curl tar zip unzip binutils xz-utils liblzo2-2 cabextract iproute2 net-tools netcat telnet \
    libatomic1 libsdl1.2debian libsdl2-2.0-0 libfontconfig libicu67 icu-devtools libunwind8 libssl-dev sqlite3 libsqlite3-dev libmariadbclient-dev-compat libduktape205 \
    locales ffmpeg gnupg2 apt-transport-https software-properties-common ca-certificates liblua5.3-0 libz-dev rapidjson-dev tzdata libevent-dev libzip4 libprotobuf23 libfluidsynth2 \
    libncurses5 python3 python3-pip python

# install pip for python2
WORKDIR /tmp

RUN curl -sSL https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py

RUN python2 get-pip.py

# install aiohttp
RUN pip3 install aiohttp

WORKDIR /home/container

COPY  ./entrypoint.sh /entrypoint.sh
CMD   [ "/bin/bash", "/entrypoint.sh" ]