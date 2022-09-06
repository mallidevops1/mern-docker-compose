FROM node:14-alpine3.10

LABEL version="1.0"
LABEL description="Production image for the Library MERN API"

WORKDIR /app

COPY ["package.json","package-lock.json*","npm-shrinkwrap.json*", "./"]

#RUN npm install
#RUN n 6.12.0
RUN npm install -g npm@latest
#RUN n lts
RUN npm i core-util-is
RUN npm install
#RUN sudo chown -R $(whoami) ~/.npm
#RUN sudo chown -R $(whoami) /usr/local/lib/node_modules/
#RUN cd {project-name}
COPY . .

CMD [ "npm", "run", "start" ]
