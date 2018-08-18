<!SLIDE>

# Init

* Run `kubeadm init --config /etc/kubeadm.config.yaml`
* Wait for it to finish, so I can copy the join command
* Be lazy with Ansible

### Ansible

    @@@ yaml
    ---
    - hosts: raspi[2345].pi.jeef.me

      tasks:

      - name: run kubeadm
        shell: kubeadm join 192.168.2.40:443 --token 9dllxf.4usr6c3jdb3on9d8 --discovery-token-ca-cert-hash sha256:436a7cb1ebf350a5819243b6104441d302fe39ccc132e916d1678db5ae66388a
