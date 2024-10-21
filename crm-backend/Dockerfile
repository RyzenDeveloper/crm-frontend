# Используем Node.js образ
FROM node:14

# Создаем рабочую директорию в контейнере
WORKDIR /usr/src/app

# Копируем файлы package.json и package-lock.json
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код
COPY . .

# Открываем порт для API
EXPOSE 3000

# Команда для запуска приложения
CMD ["npm", "start"]
