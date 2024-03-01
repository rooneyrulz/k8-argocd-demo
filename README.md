# K8s DEMO

**Note**: This repository contains three different application developments
    - mongo-app
    - node-app
    - qnotes

## K8s manifest files for mongo-app

* mongo-config.yaml
* mongo-secret.yaml
* mongo-deployment.yaml
* mongo-service.yaml

## K8s manifest files for node-app

* webapp-deployment.yaml
* webapp-service.yaml

## K8s manifest files for qnotes

- backend

    * config.yaml
    * secret.yaml
    * deployment.yaml
    * service.yaml

- frontned

    * config.yaml
    * deployment.yaml
    * service.yaml

## K8s commands

### start Minikube and check status

    minikube start --vm-driver=hyperkit 
    minikube status

### get minikube node's ip address

    minikube ip

### get basic info about k8s components

    kubectl get node
    kubectl get pod
    kubectl get svc
    kubectl get all

### get extended info about components

    kubectl get pod -o wide
    kubectl get node -o wide

### get detailed info about a specific component

    kubectl describe svc {svc-name}
    kubectl describe pod {pod-name}

### get application logs

    kubectl logs {pod-name}

### stop your Minikube cluster

    minikube stop

<br />

> :warning: **Known issue - Minikube IP not accessible**

If you can't access the NodePort service webapp with `MinikubeIP:NodePort`, execute the following command:

    minikube service <service-name>

<br />

#### Links

* k8s official documentation: <https://kubernetes.io/docs/home/>
* install minikube: <https://minikube.sigs.k8s.io/docs/start/>
* mongodb image on Docker Hub: <https://hub.docker.com/_/mongo>
