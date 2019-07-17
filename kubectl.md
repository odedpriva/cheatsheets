# kubectl

## kubectl Context and Configuration

1. Show Merged kubeconfig settings

- kubectl config view

2. use multiple kubeconfig files at the same time and view merged config

- KUBECONFIG=$HOME/.kube/config:$HOME/.kube/kubconfig2

3. display current-context

- `kubectl config current-context`

4. setup context

- brew install kube-ps1 - prompt for k8s context
- brew install kubectx - conetext switcher

5. display using go-template

- `kubectl get namespace -o go-template-file=/Users/odedpriva/k8s-templates/ns-lables.tmpl`


