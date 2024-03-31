# Используйте официальный образ nginx
FROM nginx:latest

# Удалите стандартную конфигурацию nginx
RUN rm /etc/nginx/conf.d/default.conf

# Удалите стандартный файл index.html
RUN rm -rf /usr/share/nginx/html/*

# Скопируйте новую конфигурацию nginx
COPY nginx.conf /etc/nginx/conf.d

# Скопируйте ваш HTML файл
COPY index.html /usr/share/nginx/html

# Говорим Docker'у, что контейнер будет слушать порт 80
EXPOSE 80

# Запускаем nginx в фоновом режиме
CMD ["nginx", "-g", "daemon off;"]
