# iaac-ansible
[![Ansible Lint](https://github.com/riccardo94p/iaac-ansible/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/riccardo94p/iaac-ansible/actions/workflows/ansible-lint.yml)

Ansible playbook to provision 2 CentOS VMs, install Docker on them and configure a Docker Swarm

## Requirements
* [VirtualBox](https://www.virtualbox.org/)
* [Ansible](https://www.ansible.com/)
* [Vagrant](https://www.vagrantup.com/)

### How to Run
`vagrant up && ansible-playbook -i hosts main.yml`

## Source Material
* Ansible From Beginner to Pro, M. Heap, Apress 2016
* [6 practices for super smooth Ansible experience](https://max.engineer/six-ansible-practices)
* [Ansible Linting with GitHub Actions CI/CD](https://www.ansible.com/blog/ansible-linting-with-github-actions)
