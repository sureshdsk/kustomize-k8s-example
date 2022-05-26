# Kustomize example

## Clone the repo
```
git clone git@github.com:sureshdsk/kustomize-k8s-example.git
cd kustomize-k8s-example
```

## Preview and apply manifests
Preview the kustomize output using `kustomize build` command. 
```
# preview output
kustomize build overlays/staging

# apply output to kubernetes
kustomize build overlays/staging | kubectl apply -f -

```

Use kustomize as kubectl plugin.

```
# preview output
kubectl kustomize overlays/staging

# apply output to kubernetes
kubectl apply -k overlays/staging
```