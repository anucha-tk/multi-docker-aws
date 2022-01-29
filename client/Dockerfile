# multi-state nginx
# state one node
FROM node:16-alpine as builder
WORKDIR "/app"
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# state two
# capy result state one to state two
FROM nginx
EXPOSE 3000
COPY ./nginx/defalut.conf /etc/nginx/conf.d/defalut.conf
COPY --from=builder /app/build /usr/share/nginx/html