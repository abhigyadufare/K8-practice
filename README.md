# Getting Started

This repo consist most of the examples of services and deployments demo in Kubernetes.

## Prerequisites

- kubectl
- minicube

### Commands

- To apply a service or deployment file to your kubernetes.
  ```sh
    kubectl apply -f <filename>
  ```
- To create a namespace
  ```sh
    kubectl create namespace <name>
  ```
- To check all the namespaces present in the environment
  ```sh
    kubectl get namespace
  ```
- To work in a particular namespace
  ```sh
     kubectl config set-context --current --namespace=<name>
  ```
- To check the pods currently running
  ```sh
    kubectl get pods
  ```
- To check log of a particular pod
  ```sh
    kubectl logs <pod-name>
  ```
- To see all the replicaset
  ```sh
    kubectl get replicaset
  ```
- To enable metrics server on minikube
  ```sh
    minicube addons enable metrics-server
  ```
- To check deployments
  ```sh
    kubectl get deployments
  ```
- To see horizontal pod autoscaler
  ```sh
    kubectl get HorizontalPodAutoscaler
  ```
- To see the description of your horizontal pod autoscaler (HPA)
  ```sh
    kubectl describe hpa <name>
  ```
- To check the running pods with their resource utilization
  ```sh
    kubectl top pods
  ```
- To delete all the pods, services and deployments in a namespace
  ```sh
    kubectl delete all --all -n <namespace>
  ```
- To check all the running services
  ```sh
    kubectl get svc
  ```
- To get into a particular deployment terminal
  ```sh
    kubectl exec -it <deployment-name> -- /bin/bash
  ```

### Pods & Services

Folder /services consists of practice files that we practiced on 7th Oct 23.

### Deployments

Folder /deployments consists of handson we performed on 8th Oct 23.
