FROM node:8 as docker-angular
WORKDIR /app
COPY package*.json ./
RUN npm install --silent
COPY . .
RUN npm run build

FROM nginx
VOLUME /var/cache/nginx
COPY --from=docker-angular app/dist/alurapic /usr/share/nginx/html
COPY ./config/nginx.conf /etc/nginx/conf.d/default.conf