# ArgoCD

Quick start 
> https://argo-cd.readthedocs.io/en/stable/

**Install Argo CD**
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

**Verify the CRDs**
```
kubectl get crd | grep argoproj.io
```

**Port Forwarding**
```
kubectl -n argocd port-forward svc/argocd-server 8443:443
```

**Login Using The CLI**

Default User: admin

Default Pswd:

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```




