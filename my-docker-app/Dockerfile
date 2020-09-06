# Production dockerfile
# Phase 1 - build the project 
FROM node:alpine AS builder
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# Phase 1 ends, Phase 2 starts
FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html

# No need of startup command as the primary cmd is the default one of the nginx image primary command
