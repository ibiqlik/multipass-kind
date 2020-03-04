# Launch instance
`multipass launch -n <name> -c 2 -d 15G -m 4G --cloud-init <profile>.yaml`
```
-c - CPU
-d - Disk
-m - Mem
```

Open shell to instance `multipass shell <name>

# Docker
`multipass launch -n <name> -c 2 -d 15G -m 4G --cloud-init docker.yaml`

# MicroK8s
`multipass launch -n <name> -c 2 -d 20G -m 4G --cloud-init microk8s.yaml`

# Kubernetes in Docker

Launch `multipass launch -n <name> -c 2 -d 20G -m 4G --cloud-init kubernetes.yaml`

## KIND

Get versions reference here: https://github.com/kubernetes-sigs/kind/releases
### K8s 1.15.7
`sudo kind create cluster --name=test --wait=60s --image="kindest/node:v1.15.7@sha256:e2df133f80ef633c53c0200114fce2ed5e1f6947477dbc83261a6a921169488d"`

### K8s 1.14.10
`sudo kind create cluster --name=test --wait=60s --image="kindest/node:v1.14.10@sha256:81ae5a3237c779efc4dda43cc81c696f88a194abcc4f8fa34f86cf674aa14977"`

## K3D

Get k3s (k8s) versions here https://github.com/rancher/k3s/releases
- `v1.17.3+k3s1` - Kubernetes v1.17.3
- `v1.0.1` - Kubernetes v1.16.3
- `v0.9.1` - Kubernetes v1.15.4
- `v0.8.1` - Kubernetes v1.14.6

```
multipass shell <name>
k3d create --name test --image rancher/k3s:<version> --wait 60
```
