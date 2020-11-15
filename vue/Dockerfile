FROM node:15.1.0-slim AS builder
WORKDIR /workspace
COPY ./hello-world/ /workspace/
RUN npm install && npm run build

FROM nginx:1.19.4-alpine
COPY  --from=builder /workspace/dist/ /usr/share/nginx/html/
