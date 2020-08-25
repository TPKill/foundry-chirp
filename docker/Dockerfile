FROM ubuntu:20.04
RUN apt-get update && apt-get dist-upgrade -y
RUN apt-get update && apt-get install -y \
    curl \
    libssl-dev \
    vim
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get update && apt-get install -y \
    unzip \
    nodejs
RUN mkdir /opt/foundryvtt && \
    mkdir /opt/foundrydata
COPY foundryvtt-0.6.5.zip /opt/foundryvtt
RUN cd /opt/foundryvtt && unzip foundryvtt-*.zip
EXPOSE 30000
WORKDIR /opt/foundryvtt
CMD [ "sh", "-c", "node resources/app/main.js --dataPath=/opt/foundrydata"]