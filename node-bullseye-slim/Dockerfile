FROM registry.cn-shanghai.aliyuncs.com/csvw/node:20-bullseye-slim AS base
RUN npm config set registry https://registry.npmmirror.com
RUN corepack enable
WORKDIR /app
RUN npm install -g pnpm
