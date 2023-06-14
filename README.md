# Voting App Kubernetes

Based on [example-voting-app-kubernetes-v2](https://github.com/mmumshad/example-voting-app-kubernetes-v2) repository with steps added

## Running locally

Deploy with:

```
kubectl create -f .
```

## Enable port forwarding

### Using Minikube

```
minikube service voting-service --url
minikube service result-service --url
```

Go to the provided minikube IP

### Not using Minikube

For voting app

```
kubectl port-forward <voting app pod name> 30004:80
```

For result app

```
kubectl port-forward <result app pod name> 30005:80
```

Go to http://127.0.0.1:30004/ for voting app

Go to http://127.0.0.1:30005 for result app
