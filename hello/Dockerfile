FROM node:20-alpine as build-stage

WORKDIR /app

COPY package*.json ./

RUN yarn install 

COPY . .

RUN yarn build


FROM nginx:stable-alpine as production-stage

COPY --from=build-stage /app/out/ /usr/share/nginx/html
COPY ./conf/nginx.conf /etc/nginx/conf.d/default.conf


EXPOSE 3000

CMD ["nginx", "-g", "daemon off;"]


