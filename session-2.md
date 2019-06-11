+ create namespace
```
kubectl create namespace yournamespace
```

+ create pod
```
kubectl run podname --image=service/{group_id}/yourimage:tag --port=8080 --namespace=yournamespace

kubectl get pods --namespace=[yournamespace]
kubectl describe pods/podname --namespace=[yournamespace]
```

+ service 配置
```
kubectl expose deployment/podname --type="NodePort" --port 8080 --namespace=[yournamespace]
//获取 NODE_PORT PORT 中大于30000的
kubectl get services

//VM_IP 为集群地址  NODE_PORT 为上述获取的地址
curl $VM_IP:$NODE_PORT
```
