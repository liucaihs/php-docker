FROM docker.io/nginx
RUN mkdir -p /var/app \
    && chown -R nginx:nginx /var/app
WORKDIR /var/app
COPY nginx.conf /etc/nginx/nginx.conf

