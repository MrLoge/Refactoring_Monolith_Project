# Use NodeJS base image
FROM node:13

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy app source
COPY . .

# Copy all other source code to work directory
ADD . /usr/src/app
# TypeScript
RUN npm run tsc

# Bind the port that the image will run on
EXPOSE 8081

# Define the Docker image's behavior at runtime
CMD ["node", "./www/server.js"]

