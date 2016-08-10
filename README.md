# Prometheus Config

## Forked from: https://github.com/infinityworksltd/prom-conf

## Summary

Simple container designed to populate prometheus configuration using dns autodiscovery, when deployed as part of the Prometheus catalog entry in Rancher.

## Description

This container is designed to operate as a data container, or 'sidekick' to Prometheus. It's used in the Prometheus catalog entry in Rancher extra to provide an auto-configuring monitoring platform.
Below, is the docker compose syntax to run this container, the expectation being this is mapped in using `volumes_from` and sidekicks.  keep in-mind this is designed around an implementation within a Rancher managed environment.

```
prom-conf:
    tty: true
    image: brutus333/prom-conf:latest
    volumes:
      - /etc/prometheus/

```

## Further Info

The prom-conf container can be found on the docker hub [here](https://hub.docker.com/r/brutus333/prom-conf/)
The catalog entry is available [here](https://github.com/brutus333/rancher-extra-catalog)
