FROM debian:bullseye

RUN apt update && apt install php-fpm php-mysqli curl -y

COPY www.conf /etc/php/7.4/fpm/pool.d/.
COPY script.sh .

RUN chmod +x script.sh

RUN mkdir -p /run/php

CMD ["./script.sh"]
