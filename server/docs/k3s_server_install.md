### Install K3S Server

Set External Database Endpoint
```
export K3S_DATASTORE_ENDPOINT="mysql://USERNAME:PASSWORD@tcp(MYSQLSERVERIP:3306)/DATABASENAME"
export K3S_DATASTORE_ENDPOINT="mysql://k3s:8YyFTdgkG8sCYH_WW@tcp(192.168.1.1:3306)/k3s"
```

Install K3S Server
Change `--tls-san` with Loadbalancer IP (nginx IP)
```
curl -sfL https://get.k3s.io | INSTALL_K3S_VERSION="v1.26.8+k3s1" sh -s - server --token sup3rs3cret --node-taint CriticalAddonsOnly=true:NoExecute --tls-san 192.168.1.1
```

Get agent token
```
cat /var/lib/rancher/k3s/server/agent-token
```