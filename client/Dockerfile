FROM node:14-alpine3.10  

LABEL version="1.0"
LABEL description="React Frontend for the Library API"

WORKDIR /app

COPY ./package.json ./

RUN npm install

COPY . .

RUN npm run build

FROM nginx
#FROM build as builder
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
#COPY --from=builder /app/build /usr/share/nginx/html

