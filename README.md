# Basic Install of Kubernetes and Contiv Networking
## standalone kubeadm deployment
### Orignal code credit goes to https://github.com/ben-st/ansible-kubeadm. I used it as a base and changed the CNI to Contiv (by Cisco).

- Requires Ansible 2.4 or newer
- Python netaddr 'pip install netaddr'
- Expects 3 ubuntu nodes (at least 16.04)
- Expects passwordless sudo

These playbooks deploy a very basic installation of kubeadm.
To use them, first edit the "inventory" file to contain the
hostnames of the machines on which you want kubeadm deployed, and edit the
group_vars/ file to set any kubeadm configuration parameters you need.

Then run the playbook, like this:

	`ansible-playbook -i inventory site.yml`


This is a very simple playbook and could serve as a starting point for more
complex projects.


