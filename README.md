# argocd-lab

Local registry
```shell
# You can now use the registry like this (example):
# 1. create a new cluster that uses this registry
k3d cluster create --registry-use k3d-registry.localhost:5000

# 2. tag an existing local image to be pushed to the registry
docker tag nginx:latest localhost:5000/mynginx:v0.1

# 3. push that image to the registry
docker push localhost:5000/mynginx:v0.1

# 4. run a pod that uses this image
kubectl run mynginx --image k3d-registry.localhost:5000/mynginx:v0.1
```

Create cluster
```shell
kind create cluster --name=argocd
```

Set current k8s context
```shell
kubectl cluster-info --context kind-argocd
```
# go-argocd-lab
