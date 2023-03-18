# Installing ArgoCD with Helm

see: [Setting up ArgoCD with Helm](https://www.arthurkoziel.com/setting-up-argocd-with-helm/)



```shell
k3d cluster create argocd -p "8081:80@loadbalancer" -s 1 -a 3
```

Get the admin password:
    kubectl get secret/argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode; echo ""



## Install

```
cd .../ArgoCD/Install
helm dep update ./argo-cd
helm upgrade --install argocd --namespace argocd-system --create-namespace ./argo-cd
```
