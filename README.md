Ansible Lab

	1. Create Ansible-Control VM (password SSH)
	2. Create 2 Ansible-Node VMs (password SSH)
	3. Create SSH keys on control  
		○ ssh-keygen
	4. Copy public key to Nodes
		○ ssh-copy-id username@remote_host
	5. Install Ansible
		○ sudo apt-add-repository ppa:ansible/ansible
		○ sudo apt update
		○ sudo apt install ansible
	6. Add the two nodes to inventory file
		○ sudo nano /etc/ansible/hosts
		○ Add the two nodes
	7. Check Inventory
		○ ansible-inventory --list -y
	8. Test Connection
		○ ansible all -m ping -u root
	9. Test ad-hoc commands
		○ ansible all -a "df -h" -u root
	10. Check nginx in both servers
		○ systemctl status nginx
	11. Run Ansible playbook to install nginx
	12. Check nginx in both servers
		○ systemctl status nginx


INVENTORY

[servers]
server1 ansible_host=x.x.x.x
server2 ansible_host=x.x.x.x

[all:vars]
ansible_python_interpreter=/usr/bin/python3
