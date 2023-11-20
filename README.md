# Ansible Desktop

This repository contains Ansible playbooks and roles for setting up a development and DevOps environment on Debian. It includes configurations for Google Chrome, Docker, JetBrains Toolbox, and a customized terminal environment.

## Prerequisites

Before you begin, you need to install Git and Ansible on your Debian machine.

### Installing Git and Ansible

Open a terminal and execute the following commands to install Git and Ansible:

```bash
sudo apt-get update
sudo apt-get install git software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt-get install ansible
```

## Cloning the Repository

Clone this repository to your local machine using:

```bash
git clone https://github.com/Ereaey/desktop
cd desktop
```

## Running the Playbook

To run the playbook, use the following command:

```bash
ansible-playbook -i hosts playbooks/setup.yml -e "user_var=username"
```

## Support

For any questions or support, please open an issue on the issue tracker of this repository.