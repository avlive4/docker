FROM debian:latest

RUN apt-get update && apt-get install -y \
    gcc \
    make \
    git \
    libpcap-dev \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get update && apt-get install -y \
    git ca-certificates && \
    #git clone https://github.com/rofl0r/multicat.git /multicat && \
    git clone https://code.videolan.org/robUx4/multicat.git /multicat && \
    cd /multicat && make

ENV PATH="/multicat:${PATH}"

ENTRYPOINT ["multicat"]