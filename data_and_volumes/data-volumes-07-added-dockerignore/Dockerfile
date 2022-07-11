FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ENV PORT 80
# sets the port ENV variable to a DEFAULT value of 80
# can also be set in CMD when running the container by using --env PORT=8000, which overwrites the default

# you can also use the .env file and use --env-filename .env (or other path) to be able to easily change these in code

EXPOSE $PORT
# expose the ENV instead of a hard coded number

# VOLUME [ "/app/node_modules" ]

CMD [ "npm", "start" ]
