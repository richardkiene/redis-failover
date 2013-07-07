## Usage Options:
-   -m    promote the redis-server to MASTER
-   -s    promote the redis-server to SLAVE
-   -k    start the redis-server and promote it to MASTER

## Configurations:

- Redis MASTER/SLAVE config: /etc/redis/redis.conf
- Keepalived config: /etc/keepalived/keepalived.conf

## How it works:

- Keepalived runs on the Redis MASTER and SLAVE servers
- The Redis MASTER binds the IP specified in keepalived.conf
- The Redis SLAVE connects to a Master server which has the IP 172.16.0.180
- Keepalived handles checking and runs a script if a server is online or offline
- This script will handle starting Redis promoting it to MASTER or SLAVE

## Note:

*This has NOT been tested in a production environment, use at your own risk*

## Copyright

Copyright (c) 2011 Alex Williams. See LICENSE for details.
