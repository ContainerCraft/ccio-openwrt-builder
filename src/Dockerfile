FROM debian:stable-slim as builder

WORKDIR /root/

ENV ORIGIN="https://github.com/containercraft/ccio-openwrt.git"
ENV BRANCH="origin-merge"
ENV openwrtVers="19.07.2"

ARG pkgList="\
             git \
             gpg \
             wget \
             gawk \
             file \
             unzip \
             fakeroot \
             subversion \
             ca-certificates \
             build-essential \
             libncurses-dev \
             libncurses6 \
             python2.7\
            "

RUN apt update \
     && apt-get install -y --no-install-recommends ${pkgList} \
     && git init

COPY src/entrypoint /root/

ENTRYPOINT ["./entrypoint.sh"]
