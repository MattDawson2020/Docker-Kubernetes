FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ARG DEFAULT_PORT=80
# sets a default port number that will work if nothing is specified in build, but you can also
# use --build-arg DEFAULT_PORT=8000 in the cmd to overwrite this, which is then not changeable 

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

# VOLUME [ "/app/node_modules" ]

CMD [ "npm", "start" ]
