#Frontend

FROM node:alpine

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apk del git && \
    rm -rf /var/lib/apt/lists/* && \
    adduser -S app && \
    chown -R app /frontend-example-docker

WORKDIR /frontend-example-docker
USER app
RUN npm install



CMD API_URL="http://localhost:8000" npm start 
EXPOSE 5000