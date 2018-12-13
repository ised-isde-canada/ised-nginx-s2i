# NGiNX Proxy

Reverse proxy for OpenShift projects in dev/uat/qa/prod.  Each environment should have it's own reverse proxy.

This allows apps to be routed through a common domain.  It also means apps don't have to expose routes unless necessary.

Each environment config is in its own branch.  The master branch contains the OpenShift templates required to setup the s2i builds and to instantiate new instances of the proxy.
