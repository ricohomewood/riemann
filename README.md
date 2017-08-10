The docker-compose.yml file is a monitoring service stack that comprises of the following:

Riemann
Graphite
Grafana

After you clone this repo note the following:

There is an NGINX layer inside the Graphite image and thus requires you to set a .htpasswd style password in the .htpass file located in the graphite/data/htpass folder.

You can generate .htpass style passwords from: http://www.htaccesstools.com/htpasswd-generator/
and copy this into your .htpasswd file.

once this has been done you can then run from within the cloned directory:

# docker-compose up -d

this will pull the layers and create the 3  containers.

These containers have persistant volume mounts into the specified directories in the yml compose file and if you trash the containers you can redeploy and the container will pick up the persisted data.

*******

The Dockerfile was used to build a custom image of Riemann on top of a openjdk image layer. It is not needed in this solution as it is auto build and published into the public docker registry at:

https://hub.docker.com/r/rhomewood/riemann/

Have fun.