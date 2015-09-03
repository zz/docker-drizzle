# docker-drizzle
drizzle is a cloud database fork from MySQL. This is the stable drizzle docker image Dockerfile.

use Debian 7 and drizzle 7.1 stable (2012 release)

Sample docker-compose.yml

``` yaml
drizzle:
    build: ./drizzle
    ports:
        - "4427:4427"
    volumes:
        - "/usr/local/var/drizzle"
    environment:
        - "LD_LIBRARY_PATH=/usr/local/lib"
    command: /usr/local/sbin/drizzled --user=drizzle --mysql-protocol.bind-address=0.0.0.0 --datadir=/usr/local/var/drizzle/ --drizzle-protocol.bind-address=0.0.0.0
```
