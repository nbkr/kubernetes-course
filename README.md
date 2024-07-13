# Kuberenetes Course

I'm currently working through the Kubernetes Class at the Linux Foundation site. Here are my notes.


## Lab environment
The course uses two VMs and demonstrates how to setup those VMs with Google. The big three are a bit
expensive for simple VMs and so far it looks like that is all thats needed.

* 3 VMs, Ubuntu, 2 CPUs, 8 GB Memory, 20GB Disk
* Private Network


## Architecture

Control-Pane for management, workers for actually running the containers.
On the wokers there are two parts:

* kublet: Manages the containers, starts them, stops them, etc.
* kube-proxy: Network configuration, exposes containers to the network, etc.


## Commands

### Management
* Reshow the command to add a worker node to the cluster:
  ```
  kubeadm token create --print-join-command
  ```

### Troubleshooting
* Status of the nodes:
  ```kubectl get nodes```

* Check status if kubernetes doesn't seem to be running:
  ```journalctl -xeu kubelet```

# Sources

* https://phoenixnap.com/kb/install-kubernetes-on-ubuntu \
  Used for setting up the lab environment using Vagrant and Ansible, see [lab](lab) subfolder
* https://github.com/SKorolchuk/kubernetes-vagrant-cluster-experiments/blob/master/disable-swap.sh \
  Swap disable commands.
* https://superuser.com/questions/846964/how-to-add-a-host-only-adapter-to-a-virtualbox-machine-via-vagrant-file-config \
  Additional network adapater for Vagrant Boxes
* https://github.com/Oefenweb/ansible-apparmor/tree/master \
  Copy & Pasted code for disabling app armor
* https://github.com/techiescamp/vagrant-kubeadm-kubernetes \
  Basically the same project as this one.
