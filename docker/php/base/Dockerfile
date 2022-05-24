FROM mlocati/php-extension-installer:1.5 AS extension-installer
FROM php:8.1.6-fpm-alpine3.15 AS php
COPY --from=extension-installer /usr/bin/install-php-extensions /usr/bin/
RUN install-php-extensions \
      intl \
    ;

LABEL org.opencontainers.image.source="https://github.com/Pararius/casco-job-interview"