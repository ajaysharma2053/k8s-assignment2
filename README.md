--------------------------------------
KUBECTL COMMANDS TO RUN MANIFESTS FILE
--------------------------------------

kubectl get nodes -o wide

kubectl cluster-info

kubectl get pods --all-namespaces -o wide

kubectl apply -f mysql-pod.yaml
kubectl apply -f mysql-service.yaml
kubectl apply -f webapp-pod.yaml
kubectl apply -f webapp-service.yaml

kubectl logs -f webapp-pod -n webapp 

kubectl apply -f mysql-replicaset.yaml
kubectl apply -f webapp-replicaset.yaml

kubectl apply -f mysql-deployment.yaml
kubectl apply -f webapp-deployment.yaml


kubectl get all -n mysql
kubectl get all -n webapp

kubectl rollout undo deployment webapp-deployment -n webapp
kubectl rollout restart deployment webapp-deployment -n webapp
