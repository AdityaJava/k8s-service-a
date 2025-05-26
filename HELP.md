# Build Docker image for service-a
docker build -t k8s-service-a:latest ./k8s-service-a

# If using kind, load the image into the kind cluster
kind load docker-image k8s-service-a

# Deploy service-a to Kubernetes
kubectl apply -f k8s-service-a-deployment.yaml
kubectl apply -f k8s-service-a-service.yaml
