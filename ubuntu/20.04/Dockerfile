FROM ubuntu:20.04

RUN apt-get update \
        && apt-get install ca-certificates -y \
        && sed -i "s@http://.*archive.ubuntu.com@https://mirrors.tuna.tsinghua.edu.cn@g" /etc/apt/sources.list \
        && sed -i "s@http://.*security.ubuntu.com@https://mirrors.tuna.tsinghua.edu.cn@g" /etc/apt/sources.list \
        && apt-get update
        
