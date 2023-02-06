## Create service account and get token
1. Apply template \
`kubectl apply -f octopus-k8s.yaml`
1. Get token for newly create service account \
`kubectl create token octopus-sa`

## Pushing package to repo
cloudsmith push helm none-5tP/testingoctopus package.tgz