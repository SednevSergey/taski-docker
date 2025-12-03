FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install

COPY . .
RUN npm run build

# Эта команда запустит встроенный сервер на Node.js, который будет раздавать
# содержимое директории /app/build на порте 8000
CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"] 
# docker run --rm -it -p 8000:8000 --name taski_frontend_test taski_frontend

