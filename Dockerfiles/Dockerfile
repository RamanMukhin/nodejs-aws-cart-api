# Base
FROM node:14-alpine3.13 as base

WORKDIR /app

# Dependencies
COPY package*.json ./
RUN npm install

# Build
WORKDIR /app
COPY . .
RUN npm run build

USER node
ENV PORT=8080
EXPOSE 8080

CMD ["node", "dist/main.js"]
