FROM node

# Create app directory
RUN mkdir /app
WORKDIR /app

# Install app dependencies
COPY package.json ./

# Install libraries
RUN npm i typescript ts-node

# Bundle app source
COPY . .

# Build dist folder
RUN npm build

EXPOSE 3001
CMD [ "npm", "run start" ]