<!SLIDE>

# Other Essential apps


## Load Balancer - metallb

* Physical hardware focused load balancer
* Gives my service a real IP on the network via BGP magic


## Reverse Proxy - traefik

* Fancy load balancer that implements Ingress rules
* Takes a service and gives it a subdomain
* Also uses LetsEncrypt for `https`
