## Pod

pod.yaml creates a pod in kubernetes

```sh
   kubectl apply -f pod.yaml
```

## Pod Demo2

We added a container to a deployment image

```sh
   kubectl set image deployment/my-deployment my-container=nginx:1.21
```

## Pod Demo6

To check whether it has been started on an external ip url, you need to start a minikube tunnel in a different terminal and keep it open

```sh
   minikube tunnel
```

and then run this in your working terminal to get the url

```sh
   minikube service <service-name> --url
```

or use this command if you're not in the default namespace

```sh
   minikube service <service-name> --url -n <namespace>
```

## Pod Demo7

This was created for the load balancer exercise but we used external resource that is why it is empty. The commands the we used are listed below

```sh
  kubectl create deployment hello-minikube1 --image=kicbase/echo-server:1.0
```

```sh
  kubectl get deployments
  kubectl get pods
```

```sh
  kubectl expose deployment hello-minikube1 --type=LoadBalancer --port=8080
```

## Commands

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
