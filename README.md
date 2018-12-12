# Shopinvader getting


## With docker-compose

This cmd will run locomotive + odoo in background

```
docker-compose up -d
```


This cmd (should be run after the first one) will start wagon and allow you to deploy a new website

```
git clone https://github.com/akretion/shopinvader-template template
```

Then run wagon

```
docker-compose run --service-port wagon
```

Then inside you can play with wagon

















For akretion started for akretion

You just need to clone the project and launch `docky up`

Your locomotive is available at : http://locomotive-shopinvader-demo.dy

Login/password are here : https://github.com/akretion/docker-locomotive-shopinvader-demo/blob/v3.4/README.md
