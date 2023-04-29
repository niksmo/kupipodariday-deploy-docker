FROM node:16-alpine AS builder

WORKDIR /app

COPY package* ./

RUN npm ci

COPY ./ ./

RUN npm run build

FROM nginx:1.23.1-alpine AS production

COPY  --from=builder /app/build/ /usr/share/nginx/html/

COPY --from=builder /app/nginx/conf.d/ /etc/nginx/conf.d/

EXPOSE 80