# k8s-jmeter-inflxudb1.1
### 一， 部署

```
 kubectl apply -f grafana.yaml
 kubectl apply -f influxdb.yaml
 kubectl apply -f heapster.yaml
```

验证

```
[root@master test]# kubectl get pod -n kube-system
NAME                                   READY   STATUS    RESTARTS   AGE
heapster-5457dfd6d7-xdh8n              1/1     Running   0          3m32s
monitoring-grafana-6d4945468f-nk4dq    1/1     Running   0          93m
monitoring-influxdb-659bdfd899-9tpnl   1/1     Running   0          93m
```

### 二，创建数据库

```
 curl -X POST 'http://192.168.31.28:30109/query?q=create+database+%22jmeter%22&db=_internal'
```



### 三， jmeter配置

图片1

### 四，Grafana数据源配置

图片2

导入模板

验证

