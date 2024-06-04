Install ArgoCD:
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

Get password:
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}"
```

Access:
```
kubectl port-forward svc/argocd-server -n argocd 8000:443
```