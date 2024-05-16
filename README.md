# Kuberenetes Course

I'm currently working through the Kubernetes Class at the Linux Foundation site. Here are my notes.


## Lab environment
The course uses two VMs and demonstrates how to setup those VMs with Google. The big three are a bit
expensive for simple VMs and so far it looks like that is all thats needed.

    * 2 VMs, Ubuntu, 2 CPUs, 8 GB Memory, 20GB Disk
    * Private Network


## Architecture

Control-Pane for management, workers for actually running the containers.
On the wokers there are two parts:

    * kublet: Manages the containers, starts them, stops them, etc.
    * kube-proxy: Network configuration, exposes containers to the network, etc.


# Sources

* https://phoenixnap.com/kb/install-kubernetes-on-ubuntu \
  Used for setting up the lab environment using Vagrant and Ansible, see (lab) subfolder
