FROM node

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

EXPOSE 80

ENV MONGODB_USERNAME=root
# default username is wrong, this will fail unless you add -e MONGODB_USERNAME=matt in the docker run command
ENV MONGODB_PASSWORD=secret
# default password is correct, will work

CMD ["npm", "start"]
