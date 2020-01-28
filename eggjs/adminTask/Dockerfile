# Dockerfile for Egg.js ad, adminTask
FROM jemimalwh/nodejs:v0
MAINTAINER Jemima Lee <jemimalwh@gmail.com>

# Web app path
WORKDIR /home/app
RUN git clone https://github.com/Jemimacat/k8s_eggjs_app.git

# Plugin Install
WORKDIR /home/app/k8s_eggjs_app
RUN npm i
RUN npm i -S egg-view-nunjucks
RUN npm i -S egg-mysql
RUN npm i -S egg-validate

# Expose Port to host
EXPOSE 7001

# Start application
CMD npm start