# Ansible EC2 Provisioning and Shutdown Automation

This project demonstrates the use of Ansible to automate the provisioning and shutdown of AWS EC2 instances. It highlights infrastructure automation, secure configuration management, and efficient resource handling using Ansible playbooks, variables, tags, and Ansible Vault.

---

## Tech Stack

- Ansible  
- AWS EC2  
- Ansible Vault (for secure variable encryption)  
- YAML (Playbooks and Inventory configuration)

---

## Project Overview

- Provisioned **three EC2 instances** remotely using Ansible:
  - **1 Amazon Linux**
  - **2 Ubuntu**
- Instances were defined and managed via a static **Ansible Inventory** file.
- Utilized **Ansible Vault** to securely manage sensitive credentials.
- Designed **modular and readable playbooks** for both provisioning and shutdown tasks.
- Implemented **tags** to selectively control task execution during provisioning.
- Applied **variables** to make playbooks more dynamic and reusable.
- Demonstrated **idempotency** by provisioning instances with the same AMI configuration, ensuring repeatable and consistent deployment.

---

## Security

- Used **Ansible Vault** to encrypt sensitive data such as AWS credentials.
- Maintained a `vault.pass` file for automated decryption during playbook execution.

---

## Learning Outcomes

Through this project, the following concepts and practices were reinforced:

- Infrastructure-as-Code (IaC) principles using Ansible
- Managing cloud infrastructure (EC2) in a declarative and repeatable manner
- Writing secure, dynamic, and modular playbooks with variables and tags
- Applying idempotency in infrastructure provisioning workflows
- Handling secrets securely using Ansible Vault for better DevSecOps practices

---

## Running the Project

### To create EC2 instances:
```bash
ansible-playbook ec2-create.yml --vault-password-file vault.pass

To shut down EC2 instances:

ansible-playbook -i inventory.ini ec2_shutdown.yml --vault-password-file vault.pass

