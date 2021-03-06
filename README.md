# OS-Hardening - Windows
## Powered by:

[![N|Solid](https://ezdevs.com.br/wp-content/uploads/2019/10/ansible-1.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Ansible is a software tool that provides simple but powerful automation for cross-platform computer support.

It can deliver the below characteristics:

- Cloud provisioning
- Configuration management
- Infra-service orchestration
- Agent-less

## Installation

This is the installation process for Ubuntu linux (20.04) as it was the O.S reference for creating this scripts:

## Installing Ansible on Ubuntu

Ubuntu builds are available in a PPA here.

To configure the PPA on your machine and install Ansible run these commands:

```sh
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo add-apt-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible
```

## Dependencies

Ansible used to come with most of needed modules right installed, however, if you receive a message related to a missing module, you cam involke the module installation through the ``` ansible-galaxy ``` command as below:


Example: Missing community.windows modules.

Command: ```ansible-galaxy collection install community.windows```.

Link: https://docs.ansible.com/ansible/latest/collections/community/windows/win_security_policy_module.html

You would also face python dependencies to involke commands using the ansible, but a quick read on the requirements of each module you would find the correct reference to proceed with.

Example:

Command: ```pip install zabbix-api```.

## Executing the OS-Hardening playbooks & roles

- First Download the repository using git clone & switch to downloaded project directory:

```sh
$ git clone https://github.com/lucasrf1984/os-hardening
$ cd os-hardening
```

- Second, define our inventory file and fill it with the target Windows systems 

```sh
$ 
$ cd os-hardening
$ vi hosts
```
After modifying the inventory file with the correct information related to your environment run the roles/playbooks with the below command:

```sh
$ cd os-hardening
$ ansible-playbook -i hosts main.yml
```

## Need Help? 

Reach me out, it will be nice to share experiences.

