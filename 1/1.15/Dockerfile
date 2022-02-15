FROM node:16-alpine

WORKDIR /usr/src/app

EXPOSE 3000

RUN apk add git && git clone https://github.com/ahfarmer/calculator.git
RUN mv calculator/* . && apk add npm && npm install

CMD npm start
