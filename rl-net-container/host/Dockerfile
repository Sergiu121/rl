FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN apt-get install -y bc
RUN apt-get install -y python3
RUN apt-get install -y git
RUN apt-get install -y wget
RUN apt-get install -y curl
RUN apt-get install -y sudo

RUN apt-get install -y iproute2
RUN apt-get install -y netcat-openbsd
RUN apt-get install -y vim
RUN apt-get install -y dnsmasq
RUN apt-get install -y iputils-ping
RUN apt-get install -y bash-completion
RUN apt-get install -y build-essential
RUN apt-get install -y iptables
RUN apt-get install -y ifupdown
RUN apt-get install -y net-tools

RUN apt-get -y clean

RUN rm -rf /var/lib/apt/lists/*

RUN /sbin/sysctl -w net.ipv4.ip_forward=1 > /dev/null 2>&1

COPY ./host/run.sh /usr/local/bin/run.sh
CMD ["run.sh"]

USER root
WORKDIR /root
