# 藍綠部署示範

## Requirement

* Kubernetes
* Istio
* Jenkins


```
apiVersion: networking.istio.io/v1alpha3
kind: DestinationRule
metadata:
  name: app
spec:
  host: app
  subsets:
  - name: blue
    labels:
      version: 1.4.1
```
