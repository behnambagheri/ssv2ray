# Shadowsocks-v2ray
ansible playbooks for deploy shadowsocks + v2ray-plugin on docker

Install ansible on control host:
on fedora: 

sudo dnf install ansible

on RHEL:

sudo yum install ansible

on CentOS:

sudo yum install epel-release

sudo yum install ansible

on Ubuntu:

sudo apt update

sudo apt install software-properties-common

sudo add-apt-repository --yes --update ppa:ansible/ansible

sudo apt install ansible

Arch Linux:

pacman -S ansible

The below requirements are needed on the host that executes this module.

ansible-galaxy collection install ansible.posix
ansible-galaxy collection install community.docker

before run playbook you must edit inventory file:

  ansible_host: IP_ADDRESS

  ansible_port: 22

  ansible_user: USER

  ansible_ssh_private_key_file: PRIVATE_KEY

  ansible_ssh_public_key_file: PUBLIC_KEY

  ansible_become: true

  ansible_ssh_common_args: '-o StrictHostKeyChecking=no'

  ansible_ssh_pass: SSH_PASSWORD

  personal_user: PERSONAL_USER

  personal_user_comment: "FULL NAME"

  personal_ssh_public_key_file: PERSONAL_PUBLIC_KEY


  project_name: PROJECT_NAME

  sshd_config_file: ./files/sshd_config

  nginx_config_file: ./files/nginx.conf

  domain_name: DOMAIN_NAME

  SHADOWSOCKS_PASSWORD: SHADOWSOCKS_PASSWORD


Run playbook with:

ansible-playbook -i inventory.yml full-config.yml  