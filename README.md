# Haproxy

Basic HAProxy image. You can use it in two ways:

1. Add own haproxy.cfg

```
FROM odaniait/docker-haproxy:latest
COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg
```

2. Use the default and proxy to a local app

By default any request will be proxied to 127.0.0.1:8080. If you add e.g. an Java Application, nginx, etc. on port 8080
haproxy will forward the request.
