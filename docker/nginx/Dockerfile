FROM nginx:1.20-alpine
RUN apk update && \
    apk upgrade curl && \
    apk upgrade zlib && \
    apk upgrade libxml2 && \
    apk upgrade ncurses && \
    apk upgrade openssl && \
    apk upgrade freetype
COPY ./docker/nginx/default.conf /etc/nginx/conf.d/default.conf
COPY ./docker/nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./src /var/www/html
ENV TZ=Asia/Tokyo
EXPOSE 80