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

## 其它

本示例中的 `Jenkinsfile` 會使用到 Timeout 及 Approval，其中錯誤抓取 (try-catch) 的功能，必需要有 Jenkins admin 審核允許方可使用。

### STEP
1. 請先執行 pipeline 觸發錯誤後，移至 `Jenkins > Manage Jenkins > In-process Script Approval` 中，選擇 `Approval`
2. 以上動作請再重復一次，直到您 `In-process Script Approval` 的畫面如下圖
![](https://imgur.com/WrzQCDh)

* https://stackoverflow.com/questions/38276341/jenkins-ci-pipeline-scripts-not-permitted-to-use-method-groovy-lang-groovyobject 
