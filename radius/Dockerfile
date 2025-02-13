FROM debian:latest

RUN apt-get update && apt-get install -y \
    freeradius \
    freeradius-utils \
    && rm -rf /var/cache/apt/*

#COPY ./freeradius.conf /etc/freeradius/

EXPOSE 1812 1813

CMD ["freeradius", "-X"]