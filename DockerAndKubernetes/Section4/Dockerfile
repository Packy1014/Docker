FROM node:alpine

WORKDIR /usr/app

# Copy package.json to avoid unnecessary rebuild after changing index.js
COPY ./package.json ./

RUN npm install

COPY ./ ./

CMD ["npm", "start"]