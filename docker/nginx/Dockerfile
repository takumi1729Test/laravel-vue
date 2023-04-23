FROM nginx:1.23.4-alpine

ENV TZ=UTC

# nginx config file
COPY ./docker/nginx/*.conf /etc/nginx/conf.d/

WORKDIR /var/www/html