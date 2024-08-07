# Labsetup

## Required Software
You'll need:

* Virtualbox
* Vagrant
* Ansible

## Setup process

* Run `vagrant up` and connect to the control node via `vagrant ssh control`.
* Run `sudo kubeadm init --control-plane-endpoint=control --upload-certs --pod-network-cidr=10.244.0.0/16` and do as the output says in regard of copying the the admin.conf file
* Install flannel `kubectl apply -f https://github.com/flannel-io/flannel/releases/latest/download/kube-flannel.yml`
* SSH to the workers using `vagrant ssh worker1` and `vagrant ssh worker2` respectivly. 
* Run the join command that kubeadm init put out to join each node. 
> [!WARNING]
> The kubeadm init prints two join commands. One for control-pane nodes, one for workers. Make sure you use the worker command.
