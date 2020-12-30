FROM node:12.18-alpine
ENV NODE_ENV=production
WORKDIR /usr/src/app
COPY package.json ./
RUN npm install 
COPY . ./
RUN npm run build


FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=0 /usr/src/app/build /usr/share/nginx/html