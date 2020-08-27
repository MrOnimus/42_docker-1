FROM debian:latest

RUN apt update -y && apt upgrade -y

RUN apt install wget bzip2 -y

RUN wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2 && \
	tar xfvj teamspeak3-server_linux_amd64-3.12.1.tar.bz2 && \
	cd teamspeak3-server_linux_amd64 && \
	./ts3server_startscript.sh start