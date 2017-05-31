FROM node:7-alpine

LABEL name="eth-netstats" version="1.0.0"

RUN apk --no-cache --update add curl git

RUN git clone https://github.com/cubedro/eth-netstats

WORKDIR /eth-netstats

RUN cd /eth-netstats &&\
    npm install -q &&\
    npm install -g -q grunt-cli &&\
    grunt

EXPOSE 3000

CMD ["npm", "start"]
