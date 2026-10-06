#Pull a base image which gives all the required tools and libraries
FROM eclipse-temurin:17-jdk-alpine

#Create a folder where the app will be stored
WORKDIR /app

#Copy the source code from your Host machine to the container
COPY /src/Main.java /app/Main.java

#Compile the application code
RUN javac Main.java

#run the application
CMD [ "java","Main" ]

