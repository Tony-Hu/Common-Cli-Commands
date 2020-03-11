# Minikube

## 1. Switch to Minikube docker host
```shell script
eval $(minikube docker-env)
```

## 2. Import local docker image to Minikube docker host
```shell script
docker save <image name> | (eval $(minikube docker-env) && docker load)
```