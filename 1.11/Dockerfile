FROM ubuntu:16.04

# Install Node
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN bash -c 'echo node -v && npm -v'

# Copy GIT-project
COPY backend-example-docker /usr/local/www/backend
WORKDIR /usr/local/www/backend

# Install NPM packages
RUN npm install

EXPOSE 8000
CMD ["npm", "start"]
