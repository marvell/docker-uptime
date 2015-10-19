FROM node:0.12

RUN set -xe && \
    mkdir /app && cd /app && \
    git clone git://github.com/fzaninotto/uptime.git . && \
    npm install && \
    npm install uptime-slack

COPY ./fs /

WORKDIR /app
ENV NODE_ENV production
EXPOSE 8082

CMD [ "node", "/app/app" ]
