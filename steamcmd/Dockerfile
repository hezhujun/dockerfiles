FROM hezhujun/ubuntu:18.04

ENV STEAMCMD_PATH=/opt/steamcmd

RUN dpkg --add-architecture i386 \
        && apt-get update \
        && apt-get install -y curl wget locales lib32gcc1 \
        && sed -i '/en_US.UTF-8/s/^# //g' /etc/locale.gen \
        && dpkg-reconfigure --frontend=noninteractive locales \
        && mkdir -p ${STEAMCMD_PATH} \
        && curl -sqL "https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz" | tar zxvf - -C ${STEAMCMD_PATH} \
        && ${STEAMCMD_PATH}/steamcmd.sh +quit

ENV LANG en_US.UTF-8
