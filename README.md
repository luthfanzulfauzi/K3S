# K3S-LightweightKubernetes
## Setup High Availability Kubernetes Cluster with K3s

In this installation I use 4 servers in total, later this cluster can grow by adding more nodes to the cluster.
- 1 Load Balancer + DB
- 2 K3S Server (Master Node)
- 1 K3s Agent

Installation used as below:
- **OS :** Rocky 8.7
- **Load Balancer :** Nginx
- **External DB :** MySQL 8.0
- **K3S version :** v1.26.9-rc1+k3s1

<p align="center">
  <a></a>Installation Diagram</a>
  <img src=k3s.drawio.png>
</p>
