# simple traefik v2.6 deployment with docker compose example

This example runs traefik as root with the docker socket mounted into the container to keep this example simple.
Doing this is not a good security practise. Be warned and know what you do!

What to do before using this example:

* chmod 600 config/acme.json
* docker-compose.yaml: change hostname 'foobar.example.invalid' to your real hostname
* docker-compose.yaml: change basic auth password!! (see comments in file)
* config/traefik.yaml: change email address 
* open each file, check it by yourself and understand what it does
