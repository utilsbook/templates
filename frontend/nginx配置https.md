# Nginx配置https

## 安装nginx

```bash
yum install nginx
```

## 修改配置文件

```bash
cd etc/nginx
vim nginx.conf
```

## 重启

```bash
nginx -s reload
```

## https Redirect配置

```conf
server {
 listen 80 default_server;
 listen [::]:80 default_server;
 server_name _;
 return 301 https://$host$request_uri;
}
```
