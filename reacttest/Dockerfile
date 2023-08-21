#use an official Node.js runtime as the base image
FROM node:18.17.1-slim
#set the working directory
WORKDIR /app
#Copy package.json and package-lock.json to the container
COPY package*.json .
#Install app dependencies
RUN npm install
#Copy app files to the container
COPY . .
#Build the app with npm
RUN npm run build
#Expose port 3000
EXPOSE 3000
#Command to start the app
CMD ["npm", "start"]
