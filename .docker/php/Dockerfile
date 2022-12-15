FROM php:8.2-fpm

# Set working directory
WORKDIR /var/www

  # Install system dependencies
RUN apt-get update && apt-get install -y \
git \
curl \
libpng-dev \
libonig-dev \
libxml2-dev \
zip \
unzip

  # Clear cache
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

  # Install PHP extensions
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Expose port 9000 and start php-fpm server
EXPOSE 9000 9003
CMD ["php-fpm"]
