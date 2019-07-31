FROM node

ADD package.json /
RUN npm install

ADD . /

ENTRYPOINT ["node", "src/server.js"]

