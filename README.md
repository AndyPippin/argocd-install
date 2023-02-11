# Installing ArgoCD with Helm

see: [Setting up ArgoCD with Helm](https://www.arthurkoziel.com/setting-up-argocd-with-helm/)



```shell
k3d cluster create argocd -p "8081:80@loadbalancer" -s 1 -a 3
```

