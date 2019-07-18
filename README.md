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






Login/password are here : https://github.com/akretion/docker-locomotive-shopinvader-demo/blob/v3.4/README.md
