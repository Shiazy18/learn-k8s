# Setup

Run the below command to create ind cluster, use the file kind-config.yml. It will create one master and 2 worker node,
Modify according to your need

Run the kind-cluster-install.sh script and add docker to user

```bash
    sudo groupadd docker
    sudo usermod -aG docker $USER
    newgrp docker
```

```bash
kind create cluster --config kind-config.yaml --name tws-kind-cluster
```

Verify the cluster

```bash

kubectl get nodes
kubectl cluster-info
```
