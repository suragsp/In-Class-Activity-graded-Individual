Project Title
Overview
Briefly describe the project and its purpose.

Setup Instructions
1. Setting up Google Cloud Platform (GCP) Cluster
bash
Copy code
gcloud init
gcloud container clusters create app --zone us-central1-a --num-nodes 2 --machine-type e2-medium --disk-size 10GB
2. Creating Kubernetes Namespaces
bash
Copy code
kubectl create namespace nginx-proxy
kubectl create namespace wordpress
kubectl create namespace mariadb
3. Deploying MariaDB
bash
Copy code
kubectl apply -f db/secret.yaml
kubectl apply -f db/deployment.yaml
kubectl apply -f db/service.yaml
4. Deploying WordPress
bash
Copy code
kubectl apply -f wordpress/deployment.yaml
kubectl apply -f wordpress/service.yaml
5. Deploying Nginx Proxy
bash
Copy code
kubectl apply -f nginx/configmap.yaml
kubectl apply -f nginx/deployment.yaml
kubectl apply -f nginx/service.yaml
