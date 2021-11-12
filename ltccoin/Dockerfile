FROM debian:bullseye
LABEL org.opencontainers.image.authors="576178421@qq.com"
ADD https://download.litecoin.org/litecoin-0.18.1/linux/litecoin-0.18.1-x86_64-linux-gnu.tar.gz /
RUN tar -xzvf litecoin-0.18.1-x86_64-linux-gnu.tar.gz --strip-components 1
COPY litecoin.conf /etc/litecoin.conf
EXPOSE 9332
VOLUME /data
CMD litecoind -conf=/etc/litecoin.conf
