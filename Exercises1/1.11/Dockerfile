FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl
RUN apt-get install -y git
RUN git clone https://github.com/docker-hy/backend-example-docker
WORKDIR /backend-example-docker
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN npm install

EXPOSE 8000
ENTRYPOINT FRONT_URL=http://localhost:5000 npm start

