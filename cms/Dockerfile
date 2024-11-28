FROM node:18

WORKDIR /var/www/cms

COPY ./adopt-cms/package.json ./
RUN npm install

COPY ./adopt-cms/ ./

EXPOSE 8080

CMD ["npm", "run", "dev"]
