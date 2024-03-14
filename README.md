pv --> pvc --> pod

minikube ssh
sudo mkdir /mnt/data
sudo sh -c "echo 'Hello from Kubernetes storage' > /mnt/data/index.html"
exit

kubectl apply -f pv.yaml

kubectl apply -f pvc.yaml

kubectl apply -f pod.yaml

kubectl get pv task-pv-volume

kubectl gey pvc task-pv-claim

kubectl get pod task-pv-pod

Referece: https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage

