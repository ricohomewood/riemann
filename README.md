The Dockerfile was used to build a custom image of Riemann on top of a openjdk image layer. This is also used as part of another monitoring stack solution over at:

https://hub.docker.com/r/rhomewood/riemann/

This have a docker-compose.yml file that will spin up as docker service comprising of:

Riemann
Graphite
Grafana

feel free to plat with that.

Have fun.