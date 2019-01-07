#New dockerfile using alpine
#Image size decreased almost 500MB from 723MB to 267MB.

FROM alpine:3.8

ENV PATH="/root/.local/bin:${PATH}"

RUN apk add --no-cache rtmpdump wget ffmpeg make \
    musl-dev  py-crypto py-lxml py-pip \
    py-setuptools python python2-dev  \
    bash curl ffmpeg gcc  php-cli \ 
    php-curl php-xml php-bcmath \
    libxml2-dev libxslt-dev && \
    adduser -S basicuser && \
    pip install --upgrade pip && \
    pip install setuptools yle-dl

WORKDIR /downloads
RUN chown basicuser .
USER basicuser
ENTRYPOINT ["yle-dl"]