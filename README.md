# ansible-lab
Quick introduction about ansible

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
		○ sudo systemctl config nginx
	11. Run Ansible playbook to install nginx
	12. Check nginx in both servers again
    ○ sudo systemctl config nginx
