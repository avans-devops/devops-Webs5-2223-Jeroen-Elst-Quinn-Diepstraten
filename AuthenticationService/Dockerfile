FROM node:alpine AS build


WORKDIR /app

# Copy the authenticationservice code and dependicies
COPY . . 

# copy the package.json from the parent directory
COPY package.json ./

# install the dependencies
RUN npm install -g npm@9.7.1

# Expose the port that the authenticationservice is listen to
EXPOSE 3015

# Run the authenticationservice
CMD ["node", "index.js", "rabbitmq-server"]
