minikube docker-env | Invoke-Expression
eval $(minikube docker-env)
docker build -t my-web-app:latest . -f docker/Dockerfile
kubectl apply -f k8s/
minikube service web-app-service