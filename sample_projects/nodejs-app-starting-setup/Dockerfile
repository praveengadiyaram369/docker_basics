# using node as base image for our custom image
FROM node    

# setting the working directory for docker project
WORKDIR /app

# copy the file to application folder -> first install the dependencies and then copy the application code
COPY package.json /app

# use RUN command to install dependencies for the project
RUN npm install 

# copy maintains the project structure where the docker file exits to a destination folder (app)
# we can also use COPY . ./
COPY . /app

# when the container gets started we want to expose the container to listen to a particular port
EXPOSE 80

# RUN is executed during the creation of the image and not at the time of container
# CMD is executed during the creation of the container and not at the time of image creation
CMD ["node", "server.js"]