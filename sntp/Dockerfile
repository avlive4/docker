FROM alpine:latest

RUN apk update && apk add --no-cache \
    chrony \
    && rm -rf /var/cache/apk/*

COPY ./chrony.conf /etc/chrony/chrony.conf

EXPOSE 123/udp

CMD ["chronyd", "-d", "-f", "/etc/chrony/chrony.conf"]