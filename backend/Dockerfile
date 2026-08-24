# FROM node:20
# ENV DB_HOST="mysql"
# EXPOSE 8080
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json . && \
#         *.js . && \
# RUN npm install
# CMD ["node", "index.js"]


FROM node:20
EXPOSE 8080
ENV DB_HOST="mysql"
RUN mkdir /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
CMD ["node", "index.js"]