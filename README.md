```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl create namespace argo-rollouts
kubectl apply -n argo-rollouts -f https://github.com/argoproj/argo-rollouts/releases/latest/download/install.yaml

kubectl apply -f .\platform-gitops\staging\project-web-dev.yaml
kubectl apply -f .\platform-gitops\dev\root-appsets-dev.yaml

kubectl apply -f .\platform-gitops\staging\project-web-staging.yaml
kubectl apply -f .\platform-gitops\staging\root-appsets-staging.yaml
```