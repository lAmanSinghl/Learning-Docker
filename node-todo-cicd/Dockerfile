#node base image
FROM node:12.2.0-alpine


#Working directory
WORKDIR /node

#Copy the source code into the container
COPY . .

#Install the depedencies
RUN npm install
RUN npm run test

#Document expected port
EXPOSE 8000

#Run the code
CMD [ "node","app.js"]
