# start with the base image/ starting point, in this case we want node
FROM node

# set the working directory that is targeted/ commands are run inside
WORKDIR /app

# choose what goes inside the image, in this case . targets everything in root directory
COPY . /app
# note second argument can actually be ., as it now refers tp /app, but this is clearer

#install your dependencies
RUN npm install

# RUN node server.js
# this can start the server, but this is wrong as it will actually start the server while trying to build the image

# ports are not exposed by default, this will allow outside access
EXPOSE 80

# command, this isn't executed when image is created, but when a container is started, so first action is to run the server
CMD ["node", "server.js"]
