FROM node:10-alpine

RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY ongraph/package*.json ./

USER node

#RUN npm install

COPY --chown=node:node . .

RUN rm -rf node_modules package-lock.json

RUN npm install

EXPOSE 3000

WORKDIR  ongraph

CMD [ "node", "app.js" ]
