FROM node:20.8-bookworm-slim
WORKDIR /project
RUN useradd -m -U -s /bin/bash appuser
COPY package.json package-lock.json ./
RUN chown -R appuser:appuser /project
USER appuser
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "./build/index.js"]


