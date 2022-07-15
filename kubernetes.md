# KUBERNETES

https://youtu.be/Reny0cTTv24

docker ps

password: tcuser

To get the list of nodes in K8s

kubectl get nodes

To check the list of pods

kubectl get pods

To check the namespace

Namespaces are used in kubernetes in order to group different resources and configuration objects.

kubectl get namespaces

To know the pods running in the namespace

kubectl get pods --namespace=kube-system

To create pods manually

kubectl run nginx --image=nginx

To get the details of the pods

kubectl describe pod nginx

You cannot connect to the node outside of the cluster.

To delete a pod

kubectl delete pod <name of pod>

kubectl delete pod nginx

To create alias - this is create temporarily and will no longer be available after a restart.

alias k="kubectl"

To create a deployment

kubectl create deployment <name of deployment> --image=<name of image>

k create deployment nginx-deployment --image=nginx
