#Backend

FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl && apt install -y git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    apt-get purge -y --auto-remove curl && \
    apt-get purge -y --auto-remove git && \
    rm -rf /var/lib/apt/lists/* 


WORKDIR /backend-example-docker
RUN npm install


CMD FRONT_URL="http://localhost" npm start
EXPOSE 8000