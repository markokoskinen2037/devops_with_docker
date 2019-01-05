#Frontend

FROM ubuntu:16.04 

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash  && \
    apt-get install -y nodejs && \ 
    apt-get install -y git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apt-get purge -y --auto-remove curl && \
    apt-get purge -y --auto-remove git && \
    rm -rf /var/lib/apt/lists/* 


# Vaihdetaan seijainniksi frontendin kansio
WORKDIR /frontend-example-docker
RUN npm install

CMD API_URL="http://localhost:8000" npm start 
EXPOSE 5000