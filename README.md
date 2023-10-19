# load-balancer-nginx

## Simple load-balancer with Nginx and Docker

How to use?

Run these commands after write the `docker-compose.yaml`.

Start the services

```
docker-compose up -d
```

Check if all was started

```
docker ps
```

Open a terminal to each instance and running the following commands:

```
// Open the terminal
docker-compose exec node1 bash

// See the logs
tail -f /var/log/nginx/host.access.log
```

Access the `http://localhost:8080/` and refresh the page sometimes and see the magic.

| NODE 1                       | NODE 2                       | NODE 3                       |
| ---------------------------- | ---------------------------- | ---------------------------- |
| ![Node 1](/assets/node1.png) | ![Node 2](/assets/node2.png) | ![Node 3](/assets/node3.png) |

### References

[[1] How to build a simple LOAD-BALANCER in your machine using NGINX + DOCKER](https://www.youtube.com/watch?v=srMW3Kt_NE0)

[[2] Nginx: do básico ao Load Balancer](https://www.youtube.com/watch?v=pPlcC5hDMCs)
