# simple traefik v2.6 deployment with docker compose example

This example runs traefik as root with the docker socket mounted into the container to keep this example simple.
Doing this is not a good security practise. Be warned and know what you do!

What to do before using this example:

* chmod 600 config/acme.json
* docker-compose.yaml: change hostname 'foobar.example.invalid' to your real hostname
* docker-compose.yaml: change basic auth password!! (see comments in file)
* config/traefik.yaml: change email address 
* open each file, check it by yourself and understand what it does

## Let's Encrypt TLS-ALPN-01 issue

Due to some changes to TLS-ALPN-01 challenge by Let's Encrypt (see https://community.letsencrypt.org/t/changes-to-tls-alpn-01-challenge-validation/170427) on 2022-01-26, generated certificates will be revoked on 2022-01-28.

Since this sample configuration uses TLS challenge, our created certificates are affected. To solve this issue, you have to delete the certificates in ./config/acme/acme.json
Erase the array in "Certificates" (clear everything between \[ and \] ) or clear the complete file.
After that, traefik has to be restarted.
