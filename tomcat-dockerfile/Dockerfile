FROM centos:7

MAINTAINER ashokmnr160@gmail.com

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN curl -O https://downloads.apache.org/tomcat/tomcat-8/v8.5.54/bin/apache-tomcat-8.5.54.tar.gz && \
    tar xvfz apache*.tar.gz && \
    mv apache-tomcat-8.5.54/* /opt/tomcat/. && \
    yum -y install java && \
    java -version && \
    yum -y install net-tools

WORKDIR /opt/tomcat/webapps
RUN curl -O -L https://github.com/AKSarav/SampleWebApp/raw/master/dist/SampleWebApp.war

EXPOSE 8090

CMD ["/opt/tomcat/bin/catalina.sh", "run"]