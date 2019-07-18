# Shopinvader getting started

Get a local demo of Shopinvader in a minimum of steps.

## Requirements

docker-compose https://docs.docker.com/compose/install/
git (optional, you can manually download https://raw.githubusercontent.com/akretion/shopinvader-getting-started/master/docker-compose.yml)


## Run


```bash
git clone https://github.com/akretion/shopinvader-getting-started
cd shopinvader-getting-started
docker-compose up -d
git clone https://github.com/akretion/shopinvader-template template
docker-compose run --service-port wagon
```

The following ports will be open on your host: 8069, 3000, 9200.


## Odoo ERP

Access Odoo from http://localhost:8069
Login: odoo
Password: odoo

Demo data are already loaded.

Odoo is an ERP system. It's the backend of shopinvader, where you manage products, handle sale orders, manage shipping and accounting.

## LocomotiveCMS


Login/password are here : https://github.com/akretion/docker-locomotive-shopinvader-demo/blob/v3.4/README.md
