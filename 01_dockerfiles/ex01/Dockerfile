FROM debian

MAINTAINER Brock Pace <bpace>

WORKDIR /home/teamspeak

EXPOSE 9987/udp 10011 30033

RUN apt-get -y update && apt-get upgrade -y && apt-get install -y wget bzip2
RUN wget files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_amd64-3.11.0.tar.bz2
RUN tar -xv --strip-components 1 -f  teamspeak3-server_linux_amd64-3.11.0.tar.bz2

ENTRYPOINT sh ts3server_minimal_runscript.sh license_accepted=1
