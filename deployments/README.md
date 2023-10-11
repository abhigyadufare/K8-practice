# Commands

Delete all pods, services and deployments before running the next file

```sh
    kubectl delete all --all -n <namespace>
```

## Blue Green Deployment

```sh
    kubectl apply -f green-blue-deployment.yaml
    kubectl get pods
    kubectl describe pod <pod-name>
```

## Canary Deployment

```sh
    kubectl apply -f canary-deployment.yaml
    kubectl get all
    kubectl scale deployment nginx-canary --replicas=6
    kubectl get all
```

## Empty Directory

```sh
    kubectl apply -f emptyDir.yaml
    kubectl get pods
    kubectl exec -it emptydir-demo container1 -- /bin/bash
    kubectl delete pod emptydir-demo
    kubectl get svc
    kubectl get pods
```

## Host Path

```sh
    kubectl apply -f hostpath.yaml
    kubectl get pods
    kubectl exec -it hostpath-demo container1 -- /bin/bash
    kubectl get pods
    kubectl get svc
```

## Persistent Volume

```sh
    kubectl apply -f persistentVolume.yaml
    kubectl apply -f PVC.yaml
    kubectl apply -f podUsingPV.yaml
    kubectl get pods
```

## Secret

```sh
    kubectl create secret generic my-secret1 --from-literal=username=admin --from-literal=password=pass@123
    kubectl describe secret my-secret1
    kubectl apply -f secrets.yaml
    kubectl get pods
    kubectl exec -it my-pod -- bin/bash
```

## Config Map

```sh
    kubectl apply -f configMap.yaml
    kubectl get pods
    kubectl port-forward <pod-name> 8080:80
```

## Namespace Quota

```sh
    kubectl create namespace <namespace-name>
    kubectl apply -f namespaceQuota.yaml -n <namespace-name>
    kubectl get pods
```

## Jobs

```sh
    kubectl apply -f job2.yaml
    kubectl get cronjobs
    kubectl get pods
    kubectl delete cronjobs my-cronjob
    kubectl get pods
```

## Ingress

- Install helm for this and then run commands
  ```sh
      helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
      helm install my-nginx-controller ingress-nginx/ingress-nginx
  ```
