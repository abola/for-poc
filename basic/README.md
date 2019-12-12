# Basic

參考此配置，您只需要調整檔案 `Jenkinsfile` 中，最上方的參數，如下

```pipeline
def name = "my-app"
def namespace = "my-app-project"
def imageName = "localhost:32000/my-app"
def imageTag = "1.0" // image's tag
def podReplicaCount = "3"
def serviceType = "ClusterIP" // None, NodePort, ClusterIP, LoadBalancer
def ports = "3000"
def nodePort = "" // if serviceType is NodePort
def targetPort = ""
```

調整 Image 與 Tag 至要上版的正確版號即可
