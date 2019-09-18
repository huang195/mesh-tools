# mesh-tools

Making the use of service mesh in k8s easier

# Pre-reqs

kubectl: version 1.12+
git

# Quick start

## Installation Kubectl plugin

```
wget https://raw.githubusercontent.com/huang195/mesh-tools/master/kubectl-mesh -O /usr/local/bin/kubectl-mesh && chmod 755 /usr/local/bin/kubectl-mesh
```

## Enable service mesh 

```
kubectl mesh up [--mode canary|graph|tracing]
```
Note: `graph` mode is the default mode

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

## Disable service mesh

```
kubectl mesh down
```

