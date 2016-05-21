FROM debian:testing

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 575159689BEFB442 && \
    echo 'deb http://download.fpcomplete.com/ubuntu xenial main' > /etc/apt/sources.list.d/fpco.list && \
    apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y libssl-dev stack && \
    apt-get clean

ADD app /app
WORKDIR /app

RUN stack setup
RUN stack build
