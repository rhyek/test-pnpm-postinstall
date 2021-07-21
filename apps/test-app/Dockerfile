FROM node:16-alpine as builder
# dependencies
RUN npm i -g pnpm@6.10
WORKDIR /monorepo
COPY pnpm-workspace.yaml pnpm-lock.yaml ./
COPY apps/test-app/package.json apps/test-app/
WORKDIR /monorepo/apps/test-app
# RUN pnpm i
