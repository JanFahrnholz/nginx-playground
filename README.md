# nginx-playground

This project is for testing and playing with nginx

## Basic Nginx Installation on Ubuntu

For docker just use an offical Nginx image

##### docker-compose.yml:
```
...
  image: nginx
  
```

The Nginx default config is located here: `/etc/nginx/conf.d/default.conf`

So for the first start you can just create a local config file and mount it into the container:

##### docker-compose.yml:
```
...
  volumes:
    - ./localconfig.conf:/etc/nginx/conf.d/default.conf
```
#####

If you are not using docker, simply install nginx using `apt install nginx`

#####

For more information read the full documentation [here](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/)

## Features:

- costum error pages
- IP whitelist

## Using this playground

1. Clone this repository
2. Make sure Docker and Docker-compose is installed
3. go in the project folder `cd nginx-playground/`
4. Start project using `docker-compose up -d`

**Note:** IP White/Blacklist can not be tested locally  
