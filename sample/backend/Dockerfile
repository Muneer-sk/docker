FROM node:20
ENV DB_HOST="mysql"
EXPOSE 8080
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
CMD ["node," "index.js"]

