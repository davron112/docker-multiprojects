Install docker multiprojects: author Davron Achilov
Docker project: laradock

First you need install docker
```
apt-get install docker-ce

git clone https://github.com/davron112/docker-multiprojects.git app

```
## app/laradock
```
cd laradock
```
## env.example in folder laradock
```
mv env.example .env


docker-compose build nginx mysql workspace phpmyadmin
docker-compose up build nginx mysql workspace phpmyadmin
```
if add your site to nginx ``` docker-compose nginx restart ```
add your conf multiprojects path laradock\nginx\sites\
Your projects path folder: /app/projects or in workspace: var/www
For example yii2 advanced project


## for control virtualization
```
cd laradock
docker-compose exec workspace bash
```
## test new project yii
```
cd test1 
composer create-project --prefer-dist yiisoft/yii2-app-advanced test1
php init
```
## open project

see: test1.local , backend.test1.local, test2.local

All config int .env
projects nginx: 8080
phpmyadmin port: 8980
Elasticsearch: 9200

## test configuration mysql
```
host: mysql
user: custom
pass: hSvN2yd99
```
## configuration hosts

Add domain for ubuntu
for example: ```test1.local```

Edit /etc/hosts:
```
sudo nano /etc/hosts
```
Add an entry of your domain test1.local
```
127.0.1.1       localhost
127.0.1.1       test1.local
```
Restart the hostname service:
```
sudo service hostname restart
```
and
Restart docker nginx
```
sudo docker-compose restart nginx
```
or
```
docker-compose restart nginx 
```
