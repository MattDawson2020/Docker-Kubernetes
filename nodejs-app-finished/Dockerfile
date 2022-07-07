FROM node:12

WORKDIR /app

# copy the package lock and try installing first, because this is less likely to change than the rest of your source code
COPY package.json /app

# this optimisation reduces the liklihood of having to reinstall your packages when building a new image
# doing it this way means adding a ! to some html in source code will NOT cause the package install layer to rerun, which it did in previous images
RUN npm install

COPY . /app

EXPOSE 80

CMD ["node", "server.js"]
