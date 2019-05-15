FROM ubuntu:latest

WORKDIR /mydir
RUN apt-get update && apt-get install -y git python3 python3-pip curl openjdk-8-jdk
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN rm -rf /mydir
