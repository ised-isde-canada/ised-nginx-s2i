# NGiNX Proxy

Reverse proxy for OpenShift projects in:
* dev
* uat
* qa
* prod
* intranet-dev
* intranet-uat
* intranet-qa
* intranet-prod

Non-prod environments are configured in the `non-prod` branch.  Prod config is in the `prod` branch.

This allows apps to be routed through a common domain.  It also means apps don't have to expose routes unless necessary.

When in a pod, to view the nginx config:
```
/etc/opt/rh/rh-nginx112/nginx/nginx.conf
```

Based on the [NGiNX 1.12 s2i](https://github.com/sclorg/nginx-container/tree/master/1.12) image.

## How do deploy (temp current state)
s2i builds are currently setup in openshift, but need to be manually run.
Promotion to production is done with a bamboo.
 