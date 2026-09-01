FROM node:24-slim
RUN npm i -g pnpm@10.30.3
WORKDIR /app
COPY pnpm-workspace.yaml package.json pnpm-lock.yaml ./
COPY services/web services/web
RUN pnpm install --filter web...
WORKDIR /app/services/web
CMD ["pnpm", "dev"]
