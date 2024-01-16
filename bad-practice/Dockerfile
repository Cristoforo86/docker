FROM ubuntu:latest

WORKDIR /usr/src/app

COPY package*.json /usr/src/app/package*.json

# Update the package lists and install essential packages
RUN apt-get update
RUN apt-get install -y 
RUN apt-get install curl -y 

# Install NodeJS
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt-get install -y nodejs
RUN rm -rf /var/lib/apt/lists/*
RUN npm install

COPY . /usr/src/app/

EXPOSE 3000

CMD ["node", "app.js"]
