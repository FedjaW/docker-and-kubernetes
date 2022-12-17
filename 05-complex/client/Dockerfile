FROM node:19-alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . . 
RUN npm run build

# The FROM statement is indicating the next phase is starting
# nginx - pulling the base-image from dockerhub
FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html

# The default command of the nginx container/image is to start nginx serving data.
# So we do not need to specify a command here.