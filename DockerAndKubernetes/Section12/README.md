kubectl apply -f client-pod.yaml
kubectl apply -f client–node-port.yaml
kubectl get pods -o wide
kubectl get services
minikube ip
kubectl describe pod client-pod
kubectl delete -f client-pod.yaml
kubectl apply -f client-deployment.yaml
kubectl get deployments
kubectl set image deployment/client-deployment client=stephengrider/multi-client:v5
eval $(minikube docker-env)