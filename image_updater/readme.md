# 1) Argocd-ImageUpdater
 
## Apply below stable manifest for image-updater 
```
kubectl apply -n argocd \
-f https://raw.githubusercontent.com/argoproj-labs/argocd-image-updater/v0.15.2/manifests/install.yaml

```

### if you want to delete image-updater use below manifest

```
kubectl delete -n argocd \
-f https://raw.githubusercontent.com/argoproj-labs/argocd-image-updater/v0.15.2/manifests/install.yaml

```

### In image_updater_git_secret.yaml file add your github pat and github URL and Username

[image_updater_git_secret.yaml](image_updater_git_secret.yaml)

[dockerhub-secret.yaml](dockerhub-secret.yaml)

### Im above file pass docker hub PAT, if your registry is private 

### For production use external secrets store and secrets manager to render secrets instead passing locallys