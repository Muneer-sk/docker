FROM node:20 AS build
WORKDIR /opt/server
COPY package.json . && \
     *.js .
RUN npm install

FROM node:20.18.0-alpine3.20
ENV DB_HOST="mysql"
RUN addgroup -S expense && adduser -S expense -G expense
WORKDIR /opt/server
RUN chown -R expense:expense /opt/server
COPY --from=builder /opt/server /opt/server
USER expense
CMD ["node", "index.js"]









# FROM node:20.18.0-alpine3.20
# ENV DB_HOST="mysql"
# EXPOSE 8080
# RUN addgroup -S expense && adduser -S expense -G expense
# WORKDIR /opt/server
# RUN chown -R expense:expense /opt/server
# COPY package.json . && \
#      *.js .
# RUN npm install
# USER expense
# CMD ["node", "index.js"]







# FROM node:20
# ENV DB_HOST="mysql"
# EXPOSE 8080
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD ["node", "index.js"]

