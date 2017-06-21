# OpenShift Træfik

This repository contains a dockerized version of [træfik](https://www.traefik.io)
to be used on OpenShift by running as a non-priviledged user.

## Run

    docker run -d -p 8080:8080 -p 8443:8443 -p 8081:8081 -v $PWD/etc/traefik.toml:/traefik.toml -v $PWD/certs/ca-certificates.crt:/etc/ssl/certs/ca-certificates.crt -it philippallgeuer/openshift-traefik

| Port | Protocol     |
| :------------- | :------------- |
| 8080       | http traffic |
| 8443       | https traffic (default) |
| 8081       | traefik dashobard (UI) |

## Create on openshift
