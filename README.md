# Shopinvader getting started

Get a local demo of Shopinvader in a minimum of steps.

## Requirements

docker-compose https://docs.docker.com/compose/install/

git (optional, you can manually download https://raw.githubusercontent.com/shopinvader/shopinvader-getting-started/master/docker-compose.yml)


## Run


```bash

git clone https://github.com/shopinvader/shopinvader-getting-started
cd shopinvader-getting-started
docker-compose up -d
git clone https://github.com/shopinvader/shopinvader-template template
docker-compose run --service-port wagon

```

The following ports will be open on your host: 8069, 3000, 9200.


## Odoo ERP

Access Odoo from http://odoo.localtest.me/:8069

Login: admin

Password: admin

Odoo is an ERP system. It's the backend of shopinvader, where you manage products, handle sale orders, manage shipping and do the invoicing / accounting.

## LocomotiveCMS

E-commerce website: https://locomotive.localtest.me:3000

It's the front page of the store.

CMS Admin panel http://locomotive.localtest.me:3000/locomotive

Login: demo@shopinvader.com

Password: akretion

The CMS Admin panel is used to create marketing content like a blog.
