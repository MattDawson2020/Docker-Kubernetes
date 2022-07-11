FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD [ "node", "server.js" ]

# docker run -d -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/Users/mattdawson/Projects/Docker_and_Kubernetes/data_and_volumes/data-volumes-03-adj-node-code:/app" -v /app/node_modules feedback-node:volumes# bind mount that binds the project folder to the /app, allowing changes to be more easily picked up without having to rebuild the image
# however this breaks the app because it points to a project that doesn't have the node modules
# the second volume pointing to node modules fixes this, by binding the containers node modules to a volume that overwrites the changes the porject directory tries to push
