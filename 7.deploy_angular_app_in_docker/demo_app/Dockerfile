FROM node:alpine as node

WORKDIR /src

COPY . .

RUN  npm i && npm run build


FROM nginx:alpine
COPY nginx.conf etc/nginx/nginx.conf
COPY --from=node /src/dist/demo_app /usr/share/nginx/html/demo

