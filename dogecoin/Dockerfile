FROM debian:bullseye
LABEL org.opencontainers.image.authors="576178421@qq.com"
ADD https://github.com/dogecoin/dogecoin/releases/download/v1.14.5/dogecoin-1.14.5-x86_64-linux-gnu.tar.gz /
RUN tar -xzvf dogecoin-1.14.5-x86_64-linux-gnu.tar.gz --strip-components 1
COPY dogecoin.conf /etc/dogecoin.conf
EXPOSE 22555
VOLUME /data
CMD dogecoind -conf=/etc/dogecoin.conf
