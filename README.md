# rpizero-k3s-cluster

Ansible playbooks to setup a Raspberry Pi Zero 2 W Kubernetes cluster using [k3s](https://k3s.io)

## Ansible host pre-requisites

1. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
1. Install the Ansible Docker Community collection: `ansible-galaxy collection install community.docker`
1. Install Python
1. Install the Python Docker library: `pip3 install docker`
1. Install the Python PyYaml library: `pip3 install pyyaml`
1. Install the Python docker-compose library: `pip3 install docker-compose`

## Install Procedure

1. Customize the [hosts.yaml](./hosts.yaml) file to point to your Raspberries. The "vm" host is assumed to be a single control plane node. More can be added to setup an HA control plane.
1. `make pre-requisites`
1. `make install`

## Uninstall Procedure

1. `make uninstall`

## Full documentation

The full project description is available in [my personal blog](https://www.andreveiga.dev)

## Disclaimer

The provided code was tested on a 2020 M1 Macbook Air, where the Kubernetes single control plane node was running on a VM (Ubuntu), and three Raspberry Pi Zero 2 W's acting as Kubernetes worker nodes.
