FROM ubuntu:latest
COPY . .
RUN apt update
RUN apt-get install sudo -y
RUN apt-get install curl -y
RUN curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
RUN apt-get install -y nodejs
RUN apt-get install -y build-essential
RUN npm install
EXPOSE 8080
ENTRYPOINT ["/usr/bin/node","index.js"]

