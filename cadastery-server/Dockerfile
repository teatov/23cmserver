FROM debian:stable-slim

ENV GAME_VERSION="0.0.1"

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    wget \
    unzip

WORKDIR /server

RUN wget https://git.23cmline.com/teatov/cadastery/releases/download/v${GAME_VERSION}/cadastery-${GAME_VERSION}-server.zip
RUN unzip cadastery-${GAME_VERSION}-server.zip
RUN rm cadastery-${GAME_VERSION}-server.zip

EXPOSE 10567

CMD ./cadastery-server.x86_64
