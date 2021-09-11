### steps

> build containers

```
cd nginx

docker build -t andremartds/nginx:prod -f Dockerfile.prod

cd ../laravel

docker build -t andremartds/laravel:prod . -f Dockerfile.prod

```

> create network

```
docker network create laranet

```
