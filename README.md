## Create service account and get token
1. Create env var \
`export env=uat ` env=[dev,uat,prod,pre-prod]
1. Apply template \
`helm upgrade --install  --set env=$env octopus-$env octopusChart/ `
1. Get token for newly create service account \
`kubectl create token octopus-$env-sa -n octopus-$env`

## Pushing package to repo
cloudsmith push helm none-5tP/testingoctopus package.tgz


## Exposing local K8s to Internet:
[link](https://www.indellient.com/blog/running-kubernetes-locally-using-minikube-and-ngrok/)