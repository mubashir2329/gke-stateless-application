# Stateless Application on Google Kubernetes 
In this demo I will deploy 3 deployments and services.  
1. backend master
2. backend slave
3. frontend  

## Create Project and Cluster    
First of all go to GCP and create a new project or use existing one.  
Enable Google Kubernetes API. Then go to GKE Clusters.  
Create a standard cluster with default configuration.  
Open cloud shell or set up and configure cloud sdk on local machine.  
Configure to use correct project.  
```
gcloud config set project PROJECT_NAME
```  

###  Configure gcloud to use our cluster  
```
gcloud container clusters get-credentials CLUSTER_NAME --zone=ZONE
```  
##  Create Backend Deployment/Service  
The commands for creating deployment and services using yaml file is:  
```
kubectl apply -f FILENAME.yaml
```

To check the deployment:
```
kubectl get deployments
```   
To get details of specific deployment:
```
kubectl describe deployments DEPLOYMENT_NAME
```  

If there is issue with the deployment, like its taking too long, you can check the pods that if they have been created or is there an issue, use:  
```
kubectl get pods
```  

To create/see services, same pattern, use:  
```
kubectl apply -f FILENAME.yaml  
kubectl get services
```

Now to deploy this application, go over following steps:  
1. Deploy redis-master-depoyment.yaml
2. Create redis-master-deplpymentyaml
3. redis-slave-deployment.yaml
4. redis-slave-service.yaml
5. frontend-deployment.yaml
6. frontend-service.yaml

*You can examine yaml files for more understanding*



