<!SLIDE>

# Running pods

    @@@ Console
    pi-images on  master [!] via 💎 v2.5.1
    ➜ kubectl get pods --all-namespaces
    NAMESPACE     NAME                             READY     STATUS    RESTARTS   AGE
    kube-system   coredns-78fcdf6894-d92gk         1/1       Pending   0          15m
    kube-system   coredns-78fcdf6894-m52lz         1/1       Pending   0          15m
    kube-system   etcd-raspi1                      1/1       Running   0          15m
    kube-system   kube-apiserver-raspi1            1/1       Running   0          15m
    kube-system   kube-controller-manager-raspi1   1/1       Running   0          15m
    kube-system   kube-proxy-5rpj2                 1/1       Running   0          15m
    kube-system   kube-proxy-g4dlm                 1/1       Running   0          15m
    kube-system   kube-proxy-mnfzj                 1/1       Running   0          15m
    kube-system   kube-proxy-qpbgf                 1/1       Running   0          15m
    kube-system   kube-proxy-wsbl7                 1/1       Running   0          15m
    kube-system   kube-scheduler-raspi1            1/1       Running   0          15m

### Networking backend

`coredns` will be pending until a network plugin is installed
