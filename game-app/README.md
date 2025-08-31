# What we'll do here

We will be creating a pod, its deployment and exposing it to public internet.

## Commands to run

### To create namespace

kubectl create -f namespace.yml

### to verify namesspace

kubectl get namespace

### to scale up/down pods

kubectl scale --replicas=5 --filename=deployment.yml -n nginx-ns


kubectl describe pod nginx-dep-6c996dc9c-82dm9 -n nginx-ns



sudo -E kubectl port-forward service/first-app -n nginx-ns 81:80 --address=0.0.0.0