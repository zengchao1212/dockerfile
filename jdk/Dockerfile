FROM centos:7.3.1611
MAINTAINER xiangyi '576178421@qq.com'
COPY jdk-8u101-linux-x64.rpm /
RUN rpm -iv jdk-8u101-linux-x64.rpm
RUN rm -f jdk-8u101-linux-x64.rpm
ENV JAVA_HOME /usr/java/jdk1.8.0_101
