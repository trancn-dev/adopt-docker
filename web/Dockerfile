FROM node:18

WORKDIR /var/www/web

COPY adopt-web/package.json adopt-web/package-lock.json ./
RUN npm install

COPY adopt-web/ ./

EXPOSE 3000

CMD ["npm", "run", "dev"]
