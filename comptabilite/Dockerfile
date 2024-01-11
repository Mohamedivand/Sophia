# Utiliser l'image PHP avec Apache
FROM php:7.4-apache

# Installer les extensions PHP nécessaires
RUN docker-php-ext-install pdo pdo_mysql

# Activer la réécriture d'URL pour Apache
RUN a2enmod rewrite

# Copier le code source dans le conteneur
COPY . /var/www/html

# Donner les permissions appropriées
RUN chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html/storage
