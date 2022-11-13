FROM node:alpine AS build
WORKDIR /app
COPY ./ui/ ./

RUN npm install -g @angular/cli && \
    npm install && \
    ng build

FROM nginx:alpine
COPY --from=build /app/dist/ui /usr/share/nginx/html