FROM node:16-alpine3.11
WORKDIR /usr/my-app
COPY . /usr/my-app
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]