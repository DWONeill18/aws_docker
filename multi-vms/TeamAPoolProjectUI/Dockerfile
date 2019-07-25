FROM node:10-alpine as build
WORKDIR /build
COPY . .
RUN NG_CLI_ANALYTICS=ci npm -g install @angular/cli
# install node dependencies
RUN NG_CLI_ANALYTICS=ci npm install
RUN ng build

FROM nginx:alpine
WORKDIR /app
EXPOSE 80
COPY --from=build /build/dist/TeamAPoolProjectUI .
COPY nginx.conf /etc/nginx/nginx.conf
