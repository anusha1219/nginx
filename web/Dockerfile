# this is my first docker file to create my apache
FROM ubuntu:18.04
MAINTAINER anusha.gunnam0411@gmail.com
# we need to update yum it is recommeded in centos and required in redhat and ubuntu etc
RUN apt-get -y update
RUN apt-get -y install tzdata
ENV TZ="Asia/Kolkata"
ADD config /opt
RUN apt-get -y install `cat /opt/packages`
ADD code /var/www/html
#ports we are running--meta data
EXPOSE 80
#environment variables declaration---Meta data
ENV BACKENDLB=test
CMD ["nginx", "-g", "daemon off;"]