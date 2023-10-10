#Première image build
FROM node:20.8-bookworm-slim AS builder
WORKDIR /build-project
USER root
COPY package.json package-lock.json ./
RUN npm install
COPY . .

#Seconde image exec
FROM node:20.8-bookworm-slim AS runner
COPY --from=builder /build-project /app
RUN useradd -m -U -s /bin/bash appexec
WORKDIR /app
RUN chown -R appexec:appexec /app
USER appexec
EXPOSE 8080
CMD ["node", "./build/index.js"]


