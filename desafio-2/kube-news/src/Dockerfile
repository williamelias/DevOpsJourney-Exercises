FROM node:18.11.0

WORKDIR /code

COPY package*.json ./

RUN npm install 

COPY . .

EXPOSE 3001

CMD ["node","server.js"]