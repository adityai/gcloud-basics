# gcloud-basics

## Basics

### Who-am-I

`gcloud auth list`

### Display project name

`gcloud config list project`

### Set default compute zone

`gcloud config set compute/zone us-central1-a`

### Verify server is ready for RDP

`gcloud compute instances get-serial-port-output instance-1`

## Google Kubernetes Engine Cluster (GKE)

### Create a GKE cluster

`gcloud container clusters create [cluster-name]`

### Get authentication credentials for cluster

`gcloud container clusters get-credentials [cluster-name]`

### New deployment of hello-server app to the cluster

`kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0`

### Create a Kubernetes service (expose the cluster)

`kubectl expose deployment hello-server --type=LoadBalancer --port 8080`

### Inspect the Kubernetes service

`kubectl get service`

### Delete cluster

`gcloud container clusters delete [cluster-name]`
