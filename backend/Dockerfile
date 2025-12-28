FROM node:20
ENV DB_HOST="mysql"
RUN mkdir /opt/server
WORKDIR /opt/server
COPY *.js .
COPY package.json .
RUN npm install
CMD ["node", "index.js"]
