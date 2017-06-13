FROM ubuntu:latest

MAINTAINER liuxiaotian666 “liumd@meyacom.com”
 
WORKDIR /home

ADD ./jdk1.8.0_131 /home/jdk1.8.0_131
ADD ./apache-tomcat-9.0.0.M21 /home/apache-tomcat-9.0.0.M21
 
ENV JAVA_HOME /home/jdk1.8.0_131
ENV JRE_HOME $JAVA_HOME/jre
ENV CLASSPATH .:$JAVA_HOME/lib:$JRE_HOME/lib
ENV PATH $PATH:$JAVA_HOME/bin

ENV CATALINA_HOME /home/apache-tomcat-9.0.0.M21
ENV CATALINA_BASE /home/apache-tomcat-9.0.0.M21

EXPOSE 8080

# 赋予执行权限
RUN chmod +x /home/apache-tomcat-9.0.0.M21/bin/catalina.sh /home/apache-tomcat-9.0.0.M21/bin/startup.sh

