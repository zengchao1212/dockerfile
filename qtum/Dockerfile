FROM debian:bullseye
LABEL org.opencontainers.image.authors="576178421@qq.com"
ADD https://github.com/qtumproject/qtum/releases/download/mainnet-fastlane-v0.20.4/qtum-0.20.4-x86_64-linux-gnu.tar.gz /
RUN tar -xzvf /qtum-0.20.4-x86_64-linux-gnu.tar.gz --strip-components 1
COPY qtum.conf /etc/qtum.conf
EXPOSE 3889
VOLUME /data
CMD qtumd -conf=/etc/qtum.conf
