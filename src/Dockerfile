#FROM node:lts-alpine
FROM registry.redhat.io/ubi9/nodejs-22:latest
ENV NODE_ENV=production
WORKDIR /usr/src/app
#COPY ["package.json", "npm-shrinkwrap.json*", "./"]
#RUN npm install --location=global npm@latest
#RUN npm install --production --silent # && mv node_modules ../
COPY . .
RUN npm install
EXPOSE 8080
RUN chown -R node /usr/src/app
USER node
CMD ["npm", "start"]
