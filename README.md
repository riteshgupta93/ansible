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

## NFS SETUP
