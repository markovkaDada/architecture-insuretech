```bash
docker network create --subnet 192.168.9.0/24 --driver bridge minikube

minikube start --addons=metrics-server

kubectl apply -f deployment.yaml
kubectl apply -f hpa.yaml
kubectl apply -f service.yaml

minikube service scaletestapp-service --url

minikube dashboard

locust

minikube delete
```

kubectl get hpa

linux/arm64   linux/amd64