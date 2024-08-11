# argocd-demo
```
argocd login open-ops.com:32234
argocd cluster list
argocd cluster add default --kubeconfig  ~/.kube/knts-dev.yaml --name knts-dev
argocd cluster list
kubect apply -f root-argocd-app.yml

argocd app sync all-apps
```

References
```
https://github.com/kostis-codefresh/many-appsets-demo.git
```