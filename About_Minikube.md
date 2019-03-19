#### MacOS & Already Install brew


```bash
$ brew update
$ brew cask install minikube
$ brew install kubernetes-cli
$ minikube start --vm-driver=hyperkit
```

#### Start Crash because of not install hyperkit, So install from here:
https://github.com/kubernetes/minikube/blob/master/docs/drivers.md#hyperkit-driver

```bash
$ brew install docker-machine-driver-hyperkit
$ sudo chown root:wheel /usr/local/bin/docker-machine-driver-hyperkit && sudo chmod u+s /usr/local/bin/docker-machine-driver-hyperkit
$ minikube start --vm-driver=hyperkit
$ kubectl get pods --all-namespaces
NAMESPACE     NAME                               READY     STATUS    RESTARTS   AGE
kube-system   coredns-86c58d9df4-bmsm7           1/1       Running   0          6m
kube-system   coredns-86c58d9df4-lvjd4           1/1       Running   0          6m
kube-system   etcd-minikube                      1/1       Running   0          6m
kube-system   kube-addon-manager-minikube        1/1       Running   0          5m
kube-system   kube-apiserver-minikube            1/1       Running   0          5m
kube-system   kube-controller-manager-minikube   1/1       Running   0          5m
kube-system   kube-proxy-wsspf                   1/1       Running   0          6m
kube-system   kube-scheduler-minikube            1/1       Running   0          6m
kube-system   storage-provisioner                1/1       Running   0          6m
```
