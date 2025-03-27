# CronJobs-Kubernetes-Rancher
This repo demonstrates how to create a simple cron job that runs every 1 minute

A cron job is a scheduled job in Kubernetes that runs at a specific time or interval.

This repository demonstrates how to create a **Kubernetes CronJob** using an **Alpine Linux** container. The CronJob runs **every minute** and prints a message.  

🛠 Prerequisites  
Ensure you have the following installed:  
- **Kubernetes (`kubectl`)**  
- **A running Kubernetes cluster (Minikube, k3s, EKS, GKE, etc.)**  

Steps(Terminal):

mkdir gitcron #any directory

git clone https://github.com/LokiSahetia/CronJobs-Kubernetes-Rancher.git

cd CronJobs-Kubernetes-Rancher

kubectl create ns jobby #you can create your own namespace, just make sure you update the yaml

kubectl apply -f crony.yaml

kubectl get pods -n jobby

kubectl logs foo -n jobby  #replace foo with your pod name

Once you are done, You can delete everything

kubectl delete ns jobby
