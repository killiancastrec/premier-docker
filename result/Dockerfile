FROM node:12.18.1

WORKDIR /app
EXPOSE 80

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install

COPY . .

CMD [ "node", "server.js" ]