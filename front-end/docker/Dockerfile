FROM node:8 as node

WORKDIR /var/www
COPY package*.json ./
RUN npm install

COPY . .


EXPOSE 3000
CMD [ "npm", "start" ]