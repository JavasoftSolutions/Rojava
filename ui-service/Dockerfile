FROM node:12.14-alpine AS build

WORKDIR /dist/src/app
RUN npm cache clean --force

COPY ./ui .
RUN npm install
RUN npm run build --prod

FROM nginx:latest
COPY --from=build /dist/src/app/dist/ui /usr/share/nginx/html