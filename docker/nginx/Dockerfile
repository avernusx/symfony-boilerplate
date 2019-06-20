FROM openresty/openresty:xenial
ADD entrypoint.sh /usr/bin/entrypoint.sh
ADD nginx.conf /etc/nginx/conf/nginx.conf
ADD symfony.conf /etc/nginx/conf.d/default.conf
CMD ["entrypoint.sh"]