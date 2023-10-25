### Install NGINX

Install epel-release and update
`sudo yum install epel-release`
`sudo yum update`

Install nginx
`sudo yum install nginx`

Verify nginx installation (check version)
`sudo nginx -v`

Start nginx service
```systemctl enable nginx
systemctl start nginx
```

Test nginx service
`curl -I 127.0.0.1`

Change nginx configuration, refer to nginx.conf
`/etc/nginx/nginx.conf`
