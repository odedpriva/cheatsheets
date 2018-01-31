# kubectl

## ubectl Context and Configuration

1. Show Merged kubeconfig settings
* kubectl config view

2. use multiple kubeconfig files at the same time and view merged config
* KUBECONFIG=$HOME/.kube/config:$HOME/.kube/kubconfig2

3. display current-context
* kubectl config current-context