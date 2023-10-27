### Install K3S Server

Set External Database Endpoint
```
export K3S_DATASTORE_ENDPOINT="mysql://USERNAME:PASSWORD@tcp(MYSQLSERVERIP:3306)/DATABASENAME"
export K3S_DATASTORE_ENDPOINT="mysql://k3s:8YyFTdgkG8sCYH_WW@tcp(192.168.1.1:3306)/k3s"
```

Install K3S Server
Change `--tls-san` with Loadbalancer IP (nginx IP)
```
curl -sfL https://get.k3s.io | INSTALL_K3S_VERSION="v1.26.8+k3s1" K3S_URL=https://192.168.1.1:6443 K3S_TOKEN=K10964fdcacdd47cfb9c9755e1e3858dc4c89f418d44b8407a234d3150bdf343cac::server:sup3rs3cret sh -
```