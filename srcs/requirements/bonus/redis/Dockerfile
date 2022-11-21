FROM debian:buster

RUN apt update && apt install -y redis-server

COPY redis.conf /etc/redis/redis.conf

ENTRYPOINT ["redis-server", "/etc/redis/redis.conf"]
