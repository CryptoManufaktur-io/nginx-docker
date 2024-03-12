# Overview

Docker Compose for Nginx snapshot server

Serves files from a bind-mount in `/var/www/html`, make sure this exists and holds your files and is owned by user
id `101`.

This repo was created so we could serve blockchain snapshots and have Nginx work with our Ansible scripts. It's
unlikely to be broadly useful.

`cp default.env .env`, then `nano .env` and adjust values, particularly `DOMAIN` and `NGINX_HOST` 

Meant to be used with [central-proxy-docker](https://github.com/CryptoManufaktur-io/central-proxy-docker) for traefik.

The `./ethd` script can be used as a quick-start:

`./ethd install` brings in docker-ce, if you don't have Docker installed already.

`cp default.env .env`

`nano .env` and adjust variables as needed, particularly `DOMAIN` and `NGINX_HOST`

`./ethd up`

To update the software, run `./ethd update` and then `./ethd up`

This is Nginx Docker v1.0.0
