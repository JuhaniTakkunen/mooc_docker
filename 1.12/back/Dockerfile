FROM ubuntu:16.04

# Install Node
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN bash -c 'echo node -v && npm -v'

# Copy GIT-project
COPY backend-example-docker /usr/local/www/backend
WORKDIR /usr/local/www/backend

EXPOSE 8000
# Install NPM packages
RUN npm install

 # localhost does not with VM, https://forums.docker.com/t/how-to-use-localhost-instead-of-192-168-99-100/54098/2
ENV FRONT_URL=http://192.168.1.109:5000
CMD ["npm", "start"]
