# Kubernetes
The goal is document some approach of how use Dokcer, Kubernetes and Helm.

## Docker compose
```
docker compose up -d --build
docker compose down
```

## Kubernetes v1
Running a container from the `kubectl` command line.

- Point local Docker to Minikube
`eval $(minikube docker-env)`

```
docker compose build
kubectl run my-converter --image=temperature-converter --image-pull-policy=Never
kubectl get all
kubectl port-forward pod/my-converter 8080:80
kubectl delete pod/my-converter
```

- Reset Docker to use your local machine’s daemon
`eval $(minikube docker-env -u)`

