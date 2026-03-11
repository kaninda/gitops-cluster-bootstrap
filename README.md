# gitops-cluster-bootstrap
this is a gitops root repository with argocd to manage all argocd applications

## 1. App of Apps (Orchestration)
## 2. AppProject  (Gouvernance)
## 3. RBAC (Qui peut faire quoi)
### Notes:
il est important de noter qu'ici il faut mettre en place secret avec un mot de pass choisi
```bash
kubectl create secret generic guestbook-dev-secret -n argocd --from-literal=username=guestbook-dev --from-literal=password=guestbook123
kubectl -n argocd label secret guestbook-dev-secret argocd.argoproj.io/secret-type=cluster
```