FROM ethereum/client-go:v1.6.2

LABEL name="eth-node" version="1.0.0"

RUN apk --no-cache --update add curl git bash nodejs perl

RUN cd /root &&\
    git clone https://github.com/cubedro/eth-net-intelligence-api &&\
    cd eth-net-intelligence-api &&\
    npm install -q &&\
    npm install -g -q pm2

ADD start.sh /root/start.sh
ADD app.json /root/eth-net-intelligence-api/app.json
RUN chmod +x /root/start.sh

ENTRYPOINT /root/start.sh
