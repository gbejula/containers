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

k describe pod nginx-deployment-85c6d5f6dd-cl5wg
it gives full description of the nginx-deployment

To scale the deployments
k scale deployment nginx-deployment --replicas=5

To get the details of the pods replicas
k get pods -o wide

Note: Our local computer is external relative to kubernetes cluster

To connect to one of the pods
curl 172.17.0.5 - no response

Enter into minikube
check ip address of minikube using

minikube ip

ssh docker@192.168.59.100
psd: tcuser

curl 172.17.0.5 -- gives response

To create external ip addresses to open deployment to the world.

In kubernetes cluster, it is possible to have multiple nodes and pods could be distributed across different nodes.

To expose deployments, we use the command

k expose deployment nginx-deployment --port=8080 --target-port=80

To get the services running:

k get services or k get svc

You need to expose

cluster ip will be available only in the cluster. Cluster ip address is NOT available outside of the kubernetes cluster. You are able to access cluster ip from any node.

Learning so far:
how to create a pod
how to create deployment
how to scale deployment
how to create a service for a particular deployment.

Create a custom docker image, push it to docker hub and create deployment based on this image.

to remove deployment

k delete deployment nginx-deployment

k delete service nginx-deployment

Now we create node application and configure a web server to respond to hostname of the server

To create a service

kubectl expose deployment name --port=3000

To scale deployments

kubectl scale deployment name --replicas=required_number
