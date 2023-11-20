# Ansible-role
Creating an ansible role and a specific playbook to stop a running nginx server.

Prerequisites:
1)Ansible installed on main server.
2)All other instances configured using ssh-keygen and having id_pub_rsa of main server in their authorized_keys file.
3)All Slave servers pub;ic ip addresses mentioned in inventory file.

On main server, create a role named bittu using-

$ansible-galaxy role init bittu

This initialized a seperate role and created a bunch of directories inside "bittu" like- 

main.yaml file needs to be created inside role/tasks folder

Now run the stop.yaml using 

$ansible-playbook -i inventory stop.yaml
