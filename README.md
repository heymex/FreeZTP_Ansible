# FreeZTP_Ansible
Ansible playbook for installing FreeZTP and prerequisite Python 2 packages on a current Ubuntu system

FreeZTP is a nice little system for managing zero touch provisioning on Cisco devices.  Unfortunately it has not been maintained, and critically, has not been updated to Python 3.  I created this Ansible playbook to have a repeatable process for the installation of Python 2.7, associated pip installs, and required symlinks in the filesystem to make it all work.

To use this, first SSH to your target FreeZTP server from the Ansible control node to add it to known hosts.  Update the variables in the inventory to suit your environment (the included file is for an Ubuntu cloud image in Cisco Modeling Labs), then run 'ansible-playbook -i inventory_freeztp.txt playbook_freeztp.yml'
