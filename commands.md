# Kubernetes Debugging Commands

## Pod Status & Events
kubectl get pods
kubectl describe pod <pod-name>

## Logs
kubectl logs <pod-name>
kubectl logs <pod-name> --previous

## Cluster Capacity
kubectl describe node
kubectl top pod

## Event Timeline
kubectl get events --sort-by=.metadata.creationTimestamp