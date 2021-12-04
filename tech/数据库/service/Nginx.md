https://www.runoob.com/docker/docker-install-nginx.html

https://www.ruanyifeng.com/blog/2018/02/nginx-docker.html

docker container run \
  --rm \
  --name mynginx \
  --volume "$PWD/www/html":/usr/share/nginx/html \
  --volume "$PWD/conf":/etc/nginx \
  -p 127.0.0.2:8080:80 \
  -d \
  nginx

如果要正常退出不关闭容器，请按Ctrl+P+Q进行退出容器，这一点很重要，请牢记！

exit

```
/usr/local/webserver/nginx/sbin/nginx -t
```

```
/usr/local/webserver/nginx/sbin/nginx -s reload  
```

