# gitops-udemy

kind create cluster --config=cluster.yml
kind delete cluster
k create ns argocd
helm install argocd argo/argo-cd -n argocd

kubectl port-forward service/argocd-server -n argocd 8080:443
pass: n0wdOrC936-c5AcR

argocd repo add "https://github.com/phuoc-nh/gitops-udemy.git" --username "huuphuoc252513@gmail.com" --password ""

apply first app to argocd
k apply -f argocd/argocd.yml

kubectl config use-context CONTEXT_NAME
kubectl config set-context --current --namespace=my-namespace
helm create mychart

argocd app sync nginx	


<!-- k get svc to get port -->
<!-- k get nodes to get exposed ip -->

curl 172.22.0.4:30375/get -H "accept: application/json" -> not yet working as expected
https://stackoverflow.com/questions/62432961/how-to-use-nodeport-with-kind

kubectl exec -it api-golang-b57bd5cb6-sqv68 -n demo-app -- /bin/sh
