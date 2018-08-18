<!SLIDE>

# Config

    @@@ yaml
    ---
    apiVersion: kubeadm.k8s.io/v1alpha2
    kind: MasterConfiguration
    api:
      advertiseAddress: {{ ansible_eth0.ipv4.address }}
      bindPort: 443
    clusterName: pi.jeef.me
    networking:
      podSubnet: 10.244.0.0/16
    auditPolicy:
      logDir: /var/log/kubernetes/audit
      logMaxAge: 2
      path: ""
