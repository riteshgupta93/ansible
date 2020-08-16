# Vagrant Centos setup

Install virtualbox and vagrant on the linux machine then use the following command to spawn up three centos vms.
Edit the Vagrantfile for the static ip addresses if want for the machine else remove the ', ip address: ""' part from the file for dynamic ip allocation in bridged network

Execute the command in the current working directory.

`vagrant up`

While using above command, please provide the input to the default network interface for bridging network interface of vagrant boxes.

Use the following command to ssh inside the boxes.

`ssh -i keys/vagrant_private vagrant@<box_ip>`
