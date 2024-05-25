FROM node:20-alpine
WORKDIR /app
COPY ./app .
ENV MONGO_DB_USERNAME=admin \
    MONGO_DB_PWD=password
RUN npm install
EXPOSE 3000
CMD ["node", "server.js"]
