# Voting App Kubernetes

Based on [example-voting-app-kubernetes-v2](https://github.com/mmumshad/example-voting-app-kubernetes-v2) repository with steps added

## Running locally

Deploy with:

```
kubectl create -f .
```

### Using Minikube

```
minikube service voting-service --url
```

### Not using Minikube

Enable port forwarding for voting app

```
kubectl port-forward <voting app pod name> 30004:80
```

Enable port forwarding for result app

```
kubectl port-forward <result app pod name> 30005:80
```

Access http://127.0.0.1:30004/ for voting app

Access http://127.0.0.1:30005 for result app
