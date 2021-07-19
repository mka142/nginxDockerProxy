Create `net` network: `docker network create net`

To run others containers behind this proxy use: `--net net` or `networks: ["net"]`(docker-compose) and VIRTUAL_HOST for proxy and LETSENCRYPT_HOST for ssl as you sub.domain.com 


To debug mode set env var in letsencrypt: 
```
environment:
	- DEFAULT_EMAIL
	- ACME_CA_URI=https://acme-staging-v02.api.letsencrypt.org/directory
```

https://hub.docker.com/r/jrcs/letsencrypt-nginx-proxy-companion

https://registry.hub.docker.com/r/jwilder/nginx-proxy#!

https://github.com/nginx-proxy/acme-companion/blob/main/docs/Zero-SSL.md