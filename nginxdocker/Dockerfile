FROM nginx:latest
RUN mkdir -p /var/www/html
ENV NGINX_DESAFIO04 /etc/nginx/conf.d/default.conf
COPY ./nginx.conf NGINX_DESAFIO04
ADD ./index.html /usr/share/nginx/html/ 
EXPOSE 80
LABEL description="Imagem desafio04"


