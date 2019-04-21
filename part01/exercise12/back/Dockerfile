FROM ubuntu:16.04

EXPOSE 8000

WORKDIR /mydir
RUN apt-get update && apt-get install -y git curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN git clone https://github.com/docker-hy/backend-example-docker.git
WORKDIR /mydir/backend-example-docker
RUN npm install
CMD FRONT_URL=http://localhost:5000  npm start
