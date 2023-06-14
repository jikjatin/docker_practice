FROM node:20-alpine3.17 as builder
WORKDIR '/usr/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:1.25.1-alpine
COPY --from=builder /usr/app/build /usr/share/nginx/html

# nginx container automatically start nginx server