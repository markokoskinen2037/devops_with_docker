#Backend

FROM node:alpine

RUN apk add --no-cache curl git && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    apk del curl && \
    apk del git && \
    rm -rf /var/lib/apt/lists/* && \
    adduser -S app && \
    chown -R app /backend-example-docker/

WORKDIR /backend-example-docker
USER app
RUN npm install



CMD FRONT_URL="http://localhost" npm start
EXPOSE 8000