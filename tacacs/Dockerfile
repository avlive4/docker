FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y tacacs+

COPY tac_plus.conf /etc/tacacs+/tac_plus.conf

EXPOSE 49

ENTRYPOINT tac_plus -C /etc/tacacs+/tac_plus.conf -G -g -d 256