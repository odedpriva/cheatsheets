# kubectl

## kubectl Context and Configuration

- Show Merged kubeconfig settings

```shell
>> kubectl config view
```

- use multiple kubeconfig files at the same time and view merged config

```shell
>> KUBECONFIG=$HOME/.kube/config:$HOME/.kube/kubconfig2
```

- display current-context

```shell
>> kubectl config current-context
```

- setup context

```shell
>> brew install kube-ps1 - prompt for k8s context
>> brew install kubectx - conetext switcher
```

- display using go-template

```shell
>> kubectl get namespace -o go-template-file=/Users/odedpriva/k8s-templates/ns-lables.tmpl
```

- patch a deployment

```shell
>> kubectl patch daemonsets logspout -p '{"spec":{"template":{"metadata":{"annotations":{"date":"date +'%s'"}}}}}'
```
