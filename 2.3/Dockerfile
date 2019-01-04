#Backend

FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl && apt install -y git

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN git clone https://github.com/docker-hy/backend-example-docker.git

WORKDIR /backend-example-docker
RUN npm install


CMD FRONT_URL="http://localhost:5000" npm start
EXPOSE 8000