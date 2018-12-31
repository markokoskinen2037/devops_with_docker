FROM ubuntu:16.04 

WORKDIR /mydir 
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN apt install -y git
RUN git clone https://github.com/docker-hy/frontend-example-docker.git

# Vaihdetaan seijainniksi frontendin kansio
WORKDIR /mydir/frontend-example-docker
RUN pwd

RUN npm install
RUN apt install xsel
RUN npm install -g serve
RUN npm run build

CMD serve -s -l 5000 dist

EXPOSE 5000
