kubectl delete namespace octopus

kubectl create namespace octopus

kubectl apply -f octopus-k8s.yaml

kubectl get secret $(kubectl get serviceaccount octopus-sa -o jsonpath="{.secrets[0].name}" --namespace=octopus) -o jsonpath="{.data.token}" --namespace=octopus | base64 --decode
