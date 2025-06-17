# Ansible EC2 Provisioning & Shutdown Automation

This project demonstrates how to provision and shutdown EC2 instances on AWS using Ansible automation. It showcases infrastructure management through Ansible playbooks, variables, and secrets managed via Ansible Vault.

⸻

Tech Stack
	• Ansible
	• AWS EC2
	• Ansible Vault (for secret management)
	• YAML (Playbooks, Inventory)

⸻

Project Overview
	• Provisioned 3 EC2 instances remotely using Ansible:
	• 1 Amazon Linux
	• 2 Ubuntu
	• Managed instances via an Ansible Inventory file
	• Used Ansible Vault to securely handle sensitive credentials
	• Created modular and readable playbooks for provisioning and shutdown

 Security
	• Used Ansible Vault to encrypt AWS credentials and other sensitive variables.
	• Maintained a vault.pass file for automated decryption.

⸻

 Learning Outcome

Through this project, I’ve strengthened my skills in:
	• Infrastructure automation using Ansible
	• Secure DevOps practices with Ansible Vault
	• Managing EC2 instances programmatically
	• Writing clean, modular playbooks and inventory files

⸻

 Running the Project
 ansible-playbook ec2-create.yml --vault-password-file vault.pass
 ansible-playbook -i inventory.ini ec2_shutdown.yml --vault-password-file vault.pass
