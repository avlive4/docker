FROM debian:latest

RUN apt-get update && apt-get install -y \
    gcc \
    make \
    git \
    libpcap-dev \
    && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/jblac/mcjoin.git /mcjoin \
    && cd /mcjoin \
    && make

ENV PATH="/mcjoin:${PATH}"

ENTRYPOINT ["mcjoin"]