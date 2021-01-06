# Shopinvader getting started

Get a local demo of Shopinvader in a minimum of steps.

## Requirements

docker-compose https://docs.docker.com/compose/install/

git (optional, you can manually download https://raw.githubusercontent.com/shopinvader/shopinvader-getting-started/master/docker-compose.yml)

Port 80 should be free.

Wildcard should work on localhost


## Run


```bash

git clone https://github.com/shopinvader/shopinvader-getting-started
cd shopinvader-getting-started
docker-compose up -d
git clone https://github.com/shopinvader/shopinvader-template template
docker-compose run --service-port wagon
wagon deploy test -d -v
```

The following ports will be open on your host: 80


## Odoo ERP

Access Odoo from http://odoo.localhost

Login: admin

Password: admin

Odoo is an ERP system. It's the backend of shopinvader, where you manage products, handle sale orders, manage shipping and do the invoicing / accounting.

## LocomotiveCMS

E-commerce website: http://locomotive.localhost

It's the front page of the store.

CMS Admin panel http://locomotive.localhost/locomotive

Login: demo@shopinvader.com

Password: akretion

The CMS Admin panel is used to create marketing content like a blog.

## Wagon

Preview changes in the theme with wagon:

```sh
$ docker-compose run wagon
ubuntu@wagon $ bundle exec wagon serve 
```
Access http://wagon.localhost

Configure the environment in template/config/deploy.yml
(copy paste info from http://locomotive.localhost/locomotive Developpers > Wagon

```yaml
dev:
  host: http://locomotive.localhost
  handle: demo
  email: demo@shopinvader.com
  api_key: 1234
  ``` 

Deploy:
```sh
$ docker-compose run wagon
ubuntu@wagon $ bundle exec wagon deploy dev
```
(For the first deploy, push the data: `$ bundle exec wagon deploy dev -d` 

If you change the assets (javascript or css), you have to build then deploy:
```sh
$ cd shopinvader-template
$ docker run  --rm -v `pwd`:/usr/src/app -w /usr/src/app -it node:latest bash
root@node $ yarn
root@node $ yarn build:dev
root@node $ exit
$ cd ..
$ docker-compose run wagon
ubuntu@wagon $ bundle exec wagon deploy dev
```
