# gitops-udemy

kubectl port-forward service/argocd-server -n argocd 8080:443
argocd repo add "https://github.com/phuoc-nh/gitops-udemy.git" --username "" --password ""

kubectl config use-context CONTEXT_NAME
kubectl config set-context --current --namespace=my-namespace
helm create mychart