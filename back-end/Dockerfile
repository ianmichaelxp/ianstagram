FROM node:8 as node

WORKDIR /var/www
COPY package*.json ./
RUN npm install

COPY . .


ENTRYPOINT ["npm", "start"]
EXPOSE 3000