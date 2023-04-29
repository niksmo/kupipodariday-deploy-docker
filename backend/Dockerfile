FROM node:16-alpine AS builder

WORKDIR /app

COPY package* ./

RUN npm i

COPY ./ ./

RUN npm run build

FROM node:16-alpine AS production

WORKDIR /app

COPY package* ./

RUN npm ci --omit=dev && npm i -g pm2

COPY --from=builder /app/ecosystem.config.js /app/

COPY --from=builder /app/dist ./dist

EXPOSE 3000

CMD ["pm2-runtime", "ecosystem.config.js"]