FROM node:14.17-alpine

WORKDIR /usr/src/app

RUN apk update && npm install -g npm

ENV PATH /app/node_modules/.bin:$PATH

COPY ["package.json", "yarn.lock", "./"]

RUN npm install

COPY . .

CMD ["yarn", "start"]