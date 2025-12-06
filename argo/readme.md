```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: ech0
spec:
  destination:
    namespace: shine
    server: https://kubernetes.default.svc
  source:
    path: apps/ech0/overlays/test
    repoURL: https://github.com/PrintNow/gitops-toys.git
    targetRevision: HEAD
  sources: []
  project: shine
  syncPolicy:
    automated: null

```




```yaml

apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: mtranserver
spec:
  destination:
    namespace: shine
    server: https://kubernetes.default.svc
  source:
    path: apps/mtranserver/overlays/dev
    repoURL: https://github.com/PrintNow/gitops-toys.git
    targetRevision: HEAD
  sources: [ ]
  project: shine
  syncPolicy:
    automated: null
```