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

Download the xlr.zip and the xlr license file locally.

Extract the zip file and run the following command

`xlr_home_dir/bin/run.sh -setup`

Fill out the options asked and you will get xl-release-server.conf generated in conf directory.

Update the path of xl-release-server.conf and keystore path if created during -setup in group_vars/all.

update the xlr_inventory file with your corresponding ip

use the following command to run playbook for xlr ha setup

`ansible-playbook -i xlr_inventory.yml xlr_playbook.yml`

Access the xlr instance with ha_proxy_ip:80, credentials will be admin/Admin123

Access the ha proxy stats at ha_proxy_ip:8080/stats with creds amdin/Admin123
