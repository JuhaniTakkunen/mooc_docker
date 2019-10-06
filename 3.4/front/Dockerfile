FROM node:12-alpine

ENV API_URL=/api

# Node already installed, just download data from git (I don't wanna cp -rf... anymore for each exercise)
RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /usr/local/www && \
    apk del git

WORKDIR /usr/local/www

RUN npm install
RUN npm install -g serve
RUN npm run build && \
    chown -R node /usr/local/www

# node user already in container
USER node 

EXPOSE 5000

CMD ["serve", "-s", "-l", "5000", "dist"]
