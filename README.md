# In-Class-Activity-graded-Individual
In-Class Activity (graded) Individual
 
Gcloud init
 
Making Cluster
gcloud container clusters create  app --zone us-central1-a --num-nodes 2 --machine-type e2-medium --disk-size 10GB
 




Creating Namespaces
        kubectl create namespace nginx-proxy
        kubectl create namespace wordpress
        kubectl create namespace mariadb
 

Deploying maria db files
        kubectl apply -f db/secret.yaml
        kubectl apply -f db/deployment.yaml
        kubectl apply -f db/service.yaml
        #kubectl apply -f db/mariadb-pv.yaml
        #kubectl apply -f db/mariadb-pvc.yaml
 

Deploying wordpress files
kubectl apply -f wordpress/deployment.yaml
        kubectl apply -f wordpress/service.yaml
        #kubectl apply -f wordpress/wordpress-pv.yaml
        #kubectl apply -f wordpress/wordpress-pvc.yaml
 
        
# Deploy Nginx Proxy
        kubectl apply -f nginx/configmap.yaml
        kubectl apply -f nginx/deployment.yaml
        kubectl apply -f nginx/service.yaml
 
Checking deployment
 

 

 
Configuring wordpress
 
 
