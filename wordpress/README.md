# Docker-Compose for Wordpress

```shell
docker-compose up -d
docker-compose down
```

```shell
docker run -itd -e MYSQL_ROOT_PASSWORD=wordpress -e MYSQL_DATABASE=wordpress -e MYSQL_USER=wordpress -e MYSQL_PASSWORD=wordpress --name db mysql:5.7

docker run -itd --link db:mysql -p 8000:80 -e WORDPRESS_DB_PASSWORD=wordpress wordpress:latest

```