# WordPress-Application
Deployed WordPress App on Kubernetes Cluster

## Introduction
## Application Preview
Here is the screenshot of the application
![Screenshot 2024-11-13 110158](https://github.com/user-attachments/assets/e7793477-438e-4733-9797-a14ca07c2cd6)
![Screenshot 2024-11-13 110222](https://github.com/user-attachments/assets/549901c6-477f-4f4f-9648-bd089ea83098)

## Project Overview
Successfully deployed WordPress application on a Kubernetes cluster using a MySQL StatefulSet for database storage. This setup is designed for high availability and scalability, leveraging Persistent Volumes (PV) and Persistent Volume Claims (PVC) for data persistence.

## Setup
### Step 1: MySQL StatefulSet and Service
Created the kind cluster
Created the mysql-statefulset.yaml file to define the MySQL StatefulSet.
Configured a mysql-service.yaml file for MySQL. This internal ClusterIP Service allows WordPress to communicate with MySQL within the cluster.
### Step 2: WordPress Deployment and Service
Defined the wordpress-deployment.yaml file to set up a WordPress Deployment with replicas for high availability.
Configured the wordpress-service.yaml file to expose the WordPress application as a NodePort Service or LoadBalancer if needed.
### Step 3: Persistent Volumes and Claims
Created PV and PVC configurations for both MySQL and WordPress.
Set the appropriate storage paths in the YAML files:
   mysql-pv-pvc.yaml for MySQL data persistence.
   wordpress-pv-pvc.yaml for WordPress storage.

 ### Apply Configurations
   Run:
   ```bash
   kubectl apply -f .

Screenshot of all the pods
![Screenshot 2024-11-13 105700](https://github.com/user-attachments/assets/3f0e2e6a-f19c-487b-8ac2-dcb119716c6b)
After application is successfully deployed and all the pods are up and running and sucessfully opened the website.
