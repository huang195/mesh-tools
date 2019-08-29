# mesh-tools

Making the use of service mesh in k8s easier

# Pre-reqs

kubectl version 1.12+

# Quick start

## Installation Kubectl plugin

```
wget https://raw.githubusercontent.com/huang195/mesh-tools/master/kubectl-mesh -o /usr/local/bin/kubectl-mesh
```

## Enable service mesh 

```
kubectl mesh up [--mode debug|canary|graph]
```

## Disable service mesh

```
kubectl mesh down
```

## Instrument an app

Either for all the pods in a namespace

```
kubectl mesh enable --namespace user1
```

or for a particular pod

```
kubectl mesh enable --namespace user1 --pod pod1
```

## Un-instrument the app

Either for all the pods in a namespace
```
kubectl mesh disable --namespace user1
```

or for a particular pod

```
kubectl mesh disable --namespace user1 --pod pod1
```
