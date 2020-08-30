FROM debian:latest

RUN mkdir -p /src/app

ENV TS3SERVER_LICENSE="accept"

WORKDIR /src/app

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install wget bzip2 -y

RUN wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2 && \
	tar xfvj teamspeak3-server_linux_amd64-3.12.1.tar.bz2

WORKDIR ./teamspeak3-server_linux_amd64

EXPOSE 9987/udp 10011 30033
#  9987 default voice
# 10011 server query
# 30033 file transport

ENTRYPOINT sh ts3server_minimal_runscript.sh
