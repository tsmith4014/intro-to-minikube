#start the cluster
minikube start

#See running pods
kubectl get po -A

#Dashboard of minikube cluster
minikube dashboard

#minikube comes with kubectl so check nodes
kubectl get nodes

#Check cluster components
minikube status

# get minikube config

kubectl config view

#version check
kubectl version

#Now, kubectl to be used for everything.
#check everything
kubectl get all

#check pods
kubectl get pod

#get services list
kubectl get services
