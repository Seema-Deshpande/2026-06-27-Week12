FROM node:lts-alpine

WORKDIR /app

COPY package*.json ./

RUN npm ci --omit=dev

COPY main.js server.js db.js ./
COPY src/ ./src/

ENV PORT=8080

EXPOSE 8080

CMD ["node", "main.js"]
