برای جلوگیری از توقف کانتینر می‌توان از یک حلقه بی‌نهایت اضافه نمود:
```yaml
command:
  - sh
  - -c
  - |
    while true; do sleep 3600; done
```
یا
```yaml
command: ["sleep", "3600"]
```

بررسی فایل کانفیگ آپاچی 
```bash
apachectl configtest
apachectl restart
```
اجرای آپاچی در پیش زمینه دبیان بیس
```bash
apache2-foreground
```

آپاچی در آلپاین لینوکس
```bash
apk add openrc
httpd -k restart
httpd -D FOREGROUND
rc-service apache2 status
```

/usr/local/bin/k3s-uninstall.sh


بررسی افزونه های نصب شده پی اچ پی
kubectl exec -it <php-pod-name> -- php -m

git pull --allow-unrelated-histories origin main


مای اسکو ال
mysql -u exampleuser -pexamplepassword -h mysql -D exampledb
CREATE TABLE table_name

php:8.2-apache-alpine

/usr/local/etc/php/conf.d

chown –R www-data /var/www/html && \

#            while true; do sleep 3600; done 
# php-fpm -D && chown -R www-data:www-data /usr/local/apache2 &&
#            echo "ServerName 127.0.0.1" >> /usr/local/apache2/conf/httpd.conf &&
# apk add --no-cache curl bash nano && \
