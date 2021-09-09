## Nginx Docker

Basic configuration scheme to run Nginx over docker.

1. `mkdir /etc/nginx`
2. `mkdir /var/www && mkdir /var/www/example.com` <- `/www` is  where your websites will stay
3. `sudo chown www-data:$USER /var/www -R`
3. `cd /etc/nginx && git pull https://github.com/mury12/nginx-docker`
4. Set `.conf` file inside `conf.d` with the right domain values
5. If you want to apply SSL, remove `example.com.conf` and rename `example.ssl` to `example.com.conf`. Notice that you'll need to manually place the key file paths in the `.conf` file.
6. `docker-compose up -d`
7. To restart `docker-compose down && docker-compose up -d`

> For SSL configuration, follow `certbot certonly` instructions.
