# Istio

## Service Mesh

It's an extra layer added into the cluster to monitor and modify in real-time the traffic of the application.
Also, it can increase the security and reliability level of all ecosystem.

### Istio

Website: <a>https://istio.io</a>

It's an open source project that implements Service Mash to reduce complexity in the distributed applications management, independently of language or tech.
It can easily fix very complex issues on distributed applications

It can run on:

- Kubernetes
- Mesos
- Consul
- Nomad

#### Resources

- Traffic management
  - Gateway (in - out)
  - Load balancing
  - Timeout
  - Retry policy
  - Circiut breaker
  - Fault injection
- Observability
  - Metrics
  - Distributet tracers
  - Logs
- Secority
  - Man-in-the-middle
  - mTLS
  - AAA (Authentication, Authorization, Audit)

#### K3D

Website: <a>https://k3d.io/v5.4.6/#installation</a>

It's to help work with local kubernetes

> k3d is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.

- Creating a cluster: `k3d cluster create -p "8000:30000@loadbalancer" --agents 2`
  - Accessing p8000 will be redirected to 30000
  - "agents 2": two nodes
- Changing the context: `kubectl config use-context k3d-k3s-default`
- Getting nodes: `kubectl get nodes`
