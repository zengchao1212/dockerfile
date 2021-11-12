FROM debian:bullseye
LABEL org.opencontainers.image.authors="576178421@qq.com"
ADD https://bitcoincore.org/bin/bitcoin-core-22.0/bitcoin-22.0-x86_64-linux-gnu.tar.gz /
RUN tar -xzvf /bitcoin-22.0-x86_64-linux-gnu.tar.gz --strip-components 1
COPY bitcoin.conf /etc/bitcoin.conf
EXPOSE 8332
VOLUME /data
CMD bitcoind -conf=/etc/bitcoin.conf
