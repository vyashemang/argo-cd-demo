# argo-cd-demo
## install ArgoCD in k8s
`kubectl create namespace argocd`

`kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`

## access ArgoCD UI
`kubectl get svc -n argocd`

`kubectl port-forward svc/argocd-server 9000:443 -n argocd`

open the addrees in browser

## login with 'admin' user and below token (as in documentation):
`kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo`

you can change and delete init password

