# ansible

### Vagrant

Use the vagrant/Vagrantfile for deployment of centos machines locally.

command to run the vagrant environment

`cd vagrant && vagrant up`

### prerequisites

Setup ssh connection for the nodes.

Update group_vars/all file with proper ansible_user, ansible_password, ansible_ssh_private_key_file

Run the following command to skipping host key checking in ssh

`export ANSIBLE_HOST_KEY_CHECKING=False`

## XLR HA SETUP

update the xlr_inventory file with your corresponding ip

use the following command to run playbook for xlr ha setup

`ansible-playbook -i xlr_inventory.yml xlr_playbook.yml`

Access the xlr instance with ha_proxy ip, credentials will be admin/Admin123
