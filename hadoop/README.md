# Deploy hadoop in kubernetes

## Getting Started

To deploy hadoop cluster, execute following command:
```
$ kubectl apply -f https://raw.githubusercontent.com/NanXuejiao/kubernetes-study/master/hadoop/hadoop.yaml
```
after all pods are in `running` status, hadoop cluster is ready.

## By the way

File `origin.yaml` is the following reference provided, and put it here to just have a look,
for that it does not use any resource to manage pod. Instead `hadoop.yaml` is an update of 
`origin.yaml`, using Deployment, DaemonSet, StatefulSet to controller pod.

**NOTE:** 
The second reference below, provided another way using ReplicationController to deploy, for me
it can't running normal, although all pods is in running status. I used that but get some exceptions 
when try to run the example `wordcount`. Unfortunately I can't resolve it, maybe it's something I did wrong?

# Reference
- https://www.kubernetes.org.cn/3795.html
- https://www.jianshu.com/p/e768ab139842