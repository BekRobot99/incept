FROM debian:bullseye

RUN apt update && apt install nginx openssl -y

RUN openssl req -x509 -nodes -days 365 -newkey rsa:4096 -keyout /etc/ssl/private/nginx.key -out /etc/ssl/certs/nginx.crt -subj "/C=DE/ST=Heilbron/L=Heilbronn/O=wordpress/CN=abekri.42.fr"

COPY nginx.conf /etc/nginx/.
COPY default /etc/nginx/sites-enabled/.

CMD ["nginx", "-g", "daemon off;"]
