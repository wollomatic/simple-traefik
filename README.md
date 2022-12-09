# simple traefik v3.x deployment with docker compose example

For a sample traefik v2.x deployment see branch 'traefik2'.

This example runs traefik as root with the docker socket mounted into the container to keep this example simple.
Doing this is not a good security practise. Be warned and know what you do!

For an hardened traefik v2 example see [wollomatic/traefik2-hardened](https://github.com/wollomatic/traefik2-hardened).

What to do before using this example:

* chmod 600 config/acme.json
* docker-compose.yaml: change hostname 'foobar.example.invalid' to your real hostname
* docker-compose.yaml: change basic auth password!! (see comments in file)
* config/traefik.yaml: change email address 
* open each file, check it by yourself and understand what it does
* create a docker network named 'traefik-servicenet' (`docker network create traefik-servicenet`)
