FROM ubuntu:16.04 

WORKDIR /mydir 
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN apt install -y git
RUN git clone https://github.com/docker-hy/frontend-example-docker.git

# Vaihdetaan seijainniksi frontendin kansio
WORKDIR /mydir/frontend-example-docker
RUN npm install

CMD API_URL="http://localhost:8000" npm start 


EXPOSE 5000
