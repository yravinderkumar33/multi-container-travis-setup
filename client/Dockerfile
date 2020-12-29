FROM node:12.18-alpine
ENV NODE_ENV=production
WORKDIR /usr/src/app
COPY package.json ./
RUN npm install 
COPY . ./
CMD [ "npm", "run", "build" ]


FROM nginx
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=0 /usr/src/app /usr/share/nginx/html