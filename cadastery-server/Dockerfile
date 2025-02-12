FROM alpine:latest

ENV GAME_VERSION "0.0.1"

RUN apk update
RUN apk add --no-cache bash
RUN apk add --no-cache wget

RUN wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.31-r0/glibc-2.31-r0.apk
RUN apk add --allow-untrusted glibc-2.31-r0.apk

WORKDIR /server

RUN wget https://git.23cmline.com/teatov/cadastery/releases/download/v${GAME_VERSION}/cadastery-${GAME_VERSION}-server.zip \
    && unzip cadastery-${GAME_VERSION}-server.zip \
    && rm cadastery-${GAME_VERSION}-server.zip

EXPOSE 10567

CMD ./cadastery-server.x86_64
