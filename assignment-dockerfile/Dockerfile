# fill in the blanks to dockerize this node app
FROM node:16-bullseye-slim

EXPOSE 3000

RUN apt-get update -y && apt-get install tini

WORKDIR /app

COPY package*.json ./

RUN npm install && npm cache clean --force

COPY . .

#ENTRYPOINT ["tini", "--"]

CMD ["node", "app.js"]
