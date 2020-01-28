# Dockerfile for Node.js on Centos7
FROM centos:7
MAINTAINER Jemima Lee <jemimalwh@gmail.com>

# Software install
RUN yum -y install wget 
RUN yum -y install git 
RUN yum -y install net-tools
RUN mkdir -p /home/app
WORKDIR /home/app

# Node.js install and configure
RUN mkdir -p /usr/local/nodejs 
RUN wget https://nodejs.org/dist/v12.14.1/node-v12.14.1-linux-x64.tar.xz 
RUN xz -d node-v12.14.1-linux-x64.tar.xz 
RUN tar -xvf node-v12.14.1-linux-x64.tar
RUN rm -rf node-v12.14.1-linux-x64.tar.xz 
RUN rm -rf node-v12.14.1-linux-x64.tar
RUN mv node-v12.14.1-linux-x64 /usr/local/nodejs
RUN ln -s /usr/local/nodejs/node-v12.14.1-linux-x64/bin/* /usr/bin/
CMD ["node", "--version"] 