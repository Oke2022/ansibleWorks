# AnsibleWorks

## Overview
AnsibleWorks is a collection of Ansible playbooks and roles designed for automating server configurations, deployments, and system administration tasks. This project provides a structured approach to managing infrastructure using Ansible, simplifying repetitive tasks and ensuring consistency across multiple environments.

## Features
- Automated server provisioning and configuration
- Role-based architecture for modular playbooks
- Support for various Linux distributions
- Integration with SSH for agentless automation
- Easy customization and scalability

## Prerequisites
Before using this project, ensure you have the following installed:
- **Ansible** (Latest version recommended)
- **Python 3**
- **SSH Access** to the target machines
- **Git** (Optional, for cloning the repository)

## Installation
Clone the repository:
```sh
 git clone https://github.com/Oke2022/ansibleWorks.git
 cd ansibleWorks
```

## Usage
### 1. Update Inventory
Modify the `inventory` file to include the target servers:
```ini
[webservers]
server_name ansible_host=server_ip ansible_user=server_username ansible_ssh_private_key_file=path_to_your_server_pivate_key ansible_ssh_common_args='-o StrictHostKeyChecking=no'
server_name ansible_host=server_ip ansible_user=server_username ansible_ssh_private_key_file=path_to_your_server_pivate_key ansible_ssh_common_args='-o StrictHostKeyChecking=no'

server1.example.com
server2.example.com

[dbservers]
db1.example.com
```

### 2. Run a Playbook
To run a playbook, use the following command:
```sh
ansible-playbook -i host.ini specific_yml_file.yml
```

### 3. Create a New Role
To create a new Ansible role:
```sh
ansible-galaxy init roles/new_role
```

### 4. Test Connectivity
To verify Ansible can connect to all hosts:
```sh
ansible -i inventory all -m ping
```

## Project Structure
```
ansibleWorks/

├── roles/            # Directory for Ansible roles
│   ├── angular/       # Example role for angular setup
│   ├── apache/        # Example role for apache setup
|   ├── html/        # Example role for html setup
│   ├── php/         # Example role for php setup
├── playbooks/        # Additional playbooks
├── site.yml          # Main Ansible playbook
├── site.yml          # Main Ansible playbook
|── site.html          # Main sites
├── inventory         # Inventory file for target hosts
└── README.md         # Project documentation
```

## Contributing
Contributions are welcome! Feel free to fork the repository and submit pull requests with improvements, bug fixes, or new features.

## License
This project is licensed under the MIT License.

## Author
**Oke Joshua**

For any questions or inquiries, contact me via [GitHub](https://github.com/Oke2022).

