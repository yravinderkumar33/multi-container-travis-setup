FROM node:alpine
ENV NODE_ENV=dev
ENV REDIS_HOST=
ENV REDIS_PORT=
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install
COPY . .
CMD ["npm", "run", "start"]
