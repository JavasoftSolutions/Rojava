# Rojava
Next generation of enterprise management

_Rojava is:_
1. All team members are equal.
2. All teams are equal.
3. Self-governance.

# Documentation
_Before deployment_

Comment ssl section in nginx.conf, install certificate and uncomment ssl section in nginx.conf

_Add certficate:_

sudo docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d www.javasoft.solutions

_Renew certificate:_

sudo docker-compose run --rm certbot renew

_Deploy_

sudo docker-compose up --build -d
