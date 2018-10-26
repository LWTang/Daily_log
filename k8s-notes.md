## kubernetes

### namespace
默认情况下，相同namespace中的对象具有相同的访问控制策略。大多数Kubernetes资源（例如pod、services、replication controllers或其他）都在某些Namespace中。
* 创建
  * 命令行创建 `kubectl create namespace new-namespace`
  * 通过文件创建
```
$ cat my-namespace.yaml
apiVersion: v1
kind: Namespace
metadata:
  name: new-namespace

$ kubectl create -f ./my-namespace.yaml
```

* 删除 `kubectl delete namespaces new-namespace`
* 查看 `kubectl get namespaces`

### Pod
是kubernetes创建的最小单位，一个Pod代表集群上正在运行的一个进程。Pod提供容器的运行环境并保持容器运行状态。Pod中运行一个或多个容器，k8s直接管理Pod而不是容器，当Pod中运行多个容器时，它们共享资源。

Pods提供两种共享资源：网络和存储。每个Pod被分配一个独立的IP地址，Pod中每个容器共享网络命名空间，Pod内的容器可以使用localhost相互通信。

Kubernetes使用更高级的称为Controller的抽象层，来管理Pod实例。重启Pod中的容器跟重启Pod不是一回事。

* 查看相应namespace的pod `kubectl get pods --namespace=new-namespace`


### PVC
PersistentVolumeClaim是用户对于存储的请求，跟pod类似，pod消耗结点资源，pvc消耗存储资源。
```
kind: PersistentVolumeClaim
apiVersion: v1
metadata:
  name: myclaim
spec:
  accessModes:
    - ReadWriteOnce
  volumeMode: Filesystem
  resources:
    requests:
      storage: 8Gi
  storageClassName: slow
  selector:
    matchLabels:
      release: "stable"
    matchExpressions:
      - {key: environment, operator: In, values: [dev]}
```

### PV
Persistent Volume是管理员对集群中存储资源的一种抽象，管理员指定其大小、格式、读写方式等。
```
apiVersion: v1
kind: PersistentVolume
metadata:
  name: pv0003
spec:
  capacity:
    storage: 5Gi
  volumeMode: Filesystem
  accessModes:
    - ReadWriteOnce
  persistentVolumeReclaimPolicy: Recycle
  storageClassName: slow
  mountOptions:
    - hard
    - nfsvers=4.1
  nfs:
    path: /tmp
    server: 172.17.0.2
```