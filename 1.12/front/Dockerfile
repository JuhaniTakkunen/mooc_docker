FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs

RUN bash -c 'echo node -v && npm -v'

COPY frontend-example-docker /usr/local/www

WORKDIR /usr/local/www

EXPOSE 5000

RUN npm install
RUN npm install -g serve

 # localhost does not with VM, https://forums.docker.com/t/how-to-use-localhost-instead-of-192-168-99-100/54098/2
ENV API_URL=http://192.168.1.109:8000
RUN npm run build

CMD ["serve", "-s", "-l", "5000", "dist"]
