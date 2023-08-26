<a name="readme-top"></a>

[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- GETTING STARTED -->
## Getting Started
This repo contains Manifest files to deploy MongoDB Server and 
Mongo Express in Kubernetes cluster and Expose Mongo Express as External Service


### Installation Guide
Get Instruction for MiniKube Installation at https://minikube.sigs.k8s.io/docs/start/


### BASE64 Encodings
Encode the Secret Values into base64 with https://www.base64encode.org/



### MINIKUBE COMMANDS
Sample Commands to RUN in with minikube

* Start Cluster
  ```sh
  minikube start
  ```
* Stop Cluster
  ```sh
  minikube stop
  ```
* Pause Cluster
  ```sh
  minikube pause
  ```
* Resume Cluster
  ```sh
  minikube unpause
  ```
* Delete Cluster
  ```sh
  minikube delete
  ```
* Run External Service
  ```sh
  minikube service <service_name>
  ```


### KUBECTL COMMANDS
Sample Commands to RUN in with kubectl

* Get Kubernetes Details in Json Format
  ```sh
  kubectl version --output=json
  ```

* Get Nodes
  ```sh
  kubectl get nodes
  ```

* Get Pods
  ```sh
  kubectl get pod
  ```

* Get Pods Runtime Logs
  ```sh
  kubectl get pod --watch
  ```

* Get Replicaset
  ```sh
  kubectl get replicaset 
  ```

* Get Pod Description and Details
  ```sh
  kubectl describe pod <pod_name>  
  ```

* Get Pods
  ```sh
  kubectl get deployment 
  ```

* Create Deployment
  ```sh
  kubectl create deployment <depl_name> --image=nginx
  ```

* Edit Deployment
  ```sh
  kubectl edit deployment <depl_name>
  ```

* Delete Deployment
  ```sh
  kubectl delete deployment <depl_name>  
  ```

* Get Service
  ```sh
  kubectl get service  
  ```

* Get Service
  ```sh
  kubectl get svc
  ```

* Get ConfigMap
  ```sh
  kubectl get cm 
  ```

* Get Name Space
  ```sh
  kubectl get namespace
  ```

* Get Secret
  ```sh
  kubectl get secret   
  ```

* Get Logs of a Pod
  ```sh
  kubectl logs <pod_name>
  ```

* Run Command inside a Pod
  ```sh
  kubectl exec -it <pod_name> -- bin/bash
  ```

* Create Deployment, Secret, ConfigMap, Service
  ```sh
  kubectl apply -f <.yaml file>
  ```

* Create Deployment, Secret, ConfigMap, Service
  ```sh
  kubectl apply -f <.yaml file>
  ```

## Sequence of Running the YAML
Follow the sequence to Run and Create the Cluster in kubernetes

* Create Secret
  ```sh
  kubectl apply -f mongodb-secret.yaml
  ```

* Create ConfigMap
  ```sh
  kubectl apply -f mongodb-configmap.yaml
  ```

* Create MongoDB Deployment
  ```sh
  kubectl apply -f mongodb-deployment.yaml
  ```

* Create Mongo Express Deployment
  ```sh
  kubectl apply -f mongo-express-deployment.yaml
  ```

### Run the External Service in Browser
Open a new Terminal and run this command 
  ```sh
  minikube service mongo-express-service
  ```


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/msohaibali/mongodb-mongoexpress-manifest-kubernetes/blob/main/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/msohaibali
