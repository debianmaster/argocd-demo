# argocd-demo
```
argocd login open-ops.com:32234
argocd cluster list
argocd cluster add default --kubeconfig  ~/.kube/knts-dev.yaml --name knts-dev
argocd cluster list
argocd proj create prod-eu -d "https://kubernetes.default.svc,*" -s 'https://github.com/debianmaster/argocd-demo.git'

kubectl apply -f root-argocd-app.yml

argocd app sync all-apps
```

> References
```
https://github.com/kostis-codefresh/many-appsets-demo.git
```


## Cleanup
```
kubectl delete applicationset prod-eu-appset -n argocd
argocd proj delete prod-eu
``