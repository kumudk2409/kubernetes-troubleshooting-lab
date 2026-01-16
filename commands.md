# Kubernetes Debugging Commands

## Pod Status & Events
kubectl get pods
kubectl describe pod app

## Pod Logs
kubectl logs app
kubectl logs app --previous

## Cluster Capacity
kubectl describe node
kubectl top pod

## Event Timeline
kubectl get events --sort-by=.metadata.creationTimestamp