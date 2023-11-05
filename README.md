# Haxx PiHole

Slides and documentation on how I overengineered my PiHole at home.

## Draft

### What is Pi-hole x What is DNS

> 2 minutes

Introduction in Pi-hole, what it is, what it does, what it doesn't do.

### Installing Pi-hole

> 30 seconds

Installing Pi-hole on a Raspberry Pi.

### Moving to containers

> 1 minute

Why I moved to containers. I wanted to do some monitoring, these processes had a different set of dependencies, so
moved to containers to guarantee isolation.

### Configuration using Ansible

> 1 minute

The SD card had a lot of issues, and reconfuring the Pi-hole was a pain. I decided to use Ansible to automate the
process.

### Prometheus and Grafana

> 2 minutes

Small introduction on Prometheus and Grafana and how I use dashboards.

### Introducing an Ingress and Kubernetes

> 3 minutes

Remembering ports is hard, I also wanted SSL on everything. So I introduced Traefik. This collection of services
made me realize that everything was becoming rather complex to manage in Ansible, because of the push-based nature.
I wanted to define everything in git. One solution to achieve this is Kubernetes with a GitOps approach.

_Include quote of Kelsey Hightower on not using Kubernetes_

### Alerts

> 2 minutes

Things go down all the time, so I introduced Uptime Kuma with Gotify to send me an alert when DNS no longer resolves.

### Automatic Updates

> 30 seconds

I introduced Diun to monitor current images in the cluster and if they have updates available. Whenever an update is
available, I make 1 commit and Argo makes sure all the relevant containers are updated.

### Better monitoring

> 3 minutes

I wanted better visibility on what this container is doing. Which connections come in and which requests are going out.

#### What is eBPF

> 1 minute

What is eBPF and why does it matter

#### Cilium and Hubble

> 2 minutes

How I use Cilium and Hubble to get better visibility on what is happening in the cluster.

### Security

> 2 minutes

How I leveraged eBPF to monitor what all containers are doing and how I use Falco to detect malicious activity.

### Ad blocking on the go

> 2 minutes

I wanted to use Pi-hole on the go, so I introduced WireGuard to connect to my home network and use Pi-hole on the go.
But I didn't want to expose ports on my router, so here's a sprinkle of AWS
