FROM php:8.2-fpm

WORKDIR /var/www/html

# Cài đặt các extension và công cụ cần thiết
RUN apt-get update && apt-get install -y \
    libzip-dev zip unzip git curl \
    && docker-php-ext-install pdo pdo_mysql zip

# Cài Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Sao chép mã nguồn Laravel vào container
COPY . /var/www/html

# Chỉnh quyền cho storage và bootstrap/cache
RUN chown -R www-data:www-data /var/www/html/storage /var/www/html/bootstrap/cache

# Expose cổng PHP-FPM
EXPOSE 9000

CMD ["php-fpm"]
