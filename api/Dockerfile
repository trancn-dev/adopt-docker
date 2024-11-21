FROM php:8.2-cli

COPY . /usr/src/adopt
WORKDIR /usr/src/adpot
# Cài đặt các tiện ích cần thiết
RUN apt-get update && apt-get install -y \
    libzip-dev zip unzip git \
    && docker-php-ext-install pdo pdo_mysql

# Cài Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

EXPOSE 8000
CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]
