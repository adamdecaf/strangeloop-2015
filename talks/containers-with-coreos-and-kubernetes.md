# Managing Containers at Scale with CoreOS and Kubernetes

By Kelsey Hightower

## Questions

- How would you design your infrastructure if you could never login?

## Hello World App

> A PING/PONG app with redis

- `GET /` = `PONG`
- `GET /version`
- `GET /healthz` -> 5xx when redis is down

## Core Components

- Container
- Pod
  - Each Pod gets it's own IP
  - The API can proxy to a Pod's ip
- Replication Controllers
- Service Discovery

## Tooling

- Exec'ing into containers
- Quotas
- Balancing multiple instaces of Pods
- Native rolling updates based on ports and health checks
