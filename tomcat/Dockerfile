FROM xiangyi/centos7-oracle-jdk8:8u101
MAINTAINER xiangyi '576178421@qq.com' 
RUN yum install -y wget perl gcc make apr-devel
RUN wget https://www.openssl.org/source/openssl-1.0.2j.tar.gz
RUN tar -xzvf openssl-1.0.2j.tar.gz && rm -f openssl-1.0.2j.tar.gz
WORKDIR /openssl-1.0.2j
RUN ./config -fPIC && make && make install
WORKDIR /
RUN rm -rf openssl-1.0.2j
RUN wget http://mirrors.tuna.tsinghua.edu.cn/apache/tomcat/tomcat-8/v8.5.11/bin/apache-tomcat-8.5.11.tar.gz
RUN tar -xzvf apache-tomcat-8.5.11.tar.gz -C /usr/local && rm -f apache-tomcat-8.5.11.tar.gz 
ENV CATALINA_HOME /usr/local/apache-tomcat-8.5.11
WORKDIR $CATALINA_HOME
RUN rm -f bin/*.bat
RUN tar -xzvf bin/tomcat-native.tar.gz
WORKDIR $CATALINA_HOME/tomcat-native-1.2.10-src/native
RUN ./configure --prefix=/usr && make && make install
RUN rm -rf $CATALINA_HOME/tomcat-native-1.2.10-src
RUN rm -f $CATALINA_HOME/bin/*.tar.gz
WORKDIR $CATALINA_HOME
EXPOSE 8080
CMD ["bin/catalina.sh", "run"]
