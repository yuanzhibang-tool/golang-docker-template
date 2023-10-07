FROM golang:1.21.2-bullseye
ARG DEBIAN_FRONTEND=noninteractive
RUN echo 'start build'
RUN LC_ALL=C.UTF-8
# speed up build in China
RUN sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
RUN apt update && apt install git -y
ENV GO111MODULE=on
# speed up in China
ENV GOPROXY=https://goproxy.cn,direct
ENTRYPOINT tail -f /dev/null
