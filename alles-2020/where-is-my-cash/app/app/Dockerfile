FROM node:14-alpine

# install dependencies
COPY package.json package-lock.json /app/
WORKDIR /app
RUN npm install

# add the actual app
ADD server.js /app/
ADD ./static /app/static

USER 1000:1000

ENV BIND_ADDR=0.0.0.0 PORT=1337
CMD ["npm", "start"]
