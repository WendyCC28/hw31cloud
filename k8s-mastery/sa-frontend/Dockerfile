# build React
FROM node:16 AS build-stage
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build


# build nginx
FROM nginx:1.27-alpine
COPY --from=build-stage /app/build /usr/share/nginx/html

# Add nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

