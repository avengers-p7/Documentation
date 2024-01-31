# Ansible Role to setup Jenkins


|   Authors        |  Created on   |  Version   | Last updated by | Last edited on |
| -----------------| --------------| -----------|---------------- | -------------- |
| Vidhi Yadav      |  31 Jan 2024   |     v1     | Vidhi Yadav     | 31 Jan 2024    |


## Table of Contents
+ [Introduction](#Introduction)
+ [Pre-requisites](#pre-requisites)
+ [Setup Ansible Role](#steps)
+ [Tool Comparison](#tool-comparison)
+ [Guide to Installation](#Installing-OWASP-Dependency-Check)
+ [Best Practices](#best-practices)
+ [Security Compliance](#security-compliance)
+ [Contact Information](#contact-information)
+ [References](#references)

# Introduction
This role is designed to automate the installation and configuration of Jenkins on target servers. Whether you're setting up Jenkins for continuous integration, continuous delivery, or other purposes, this role aims to simplify the process.

## Pre-requisites

Before using this Ansible role to set up Jenkins, ensure that the following prerequisites are met:

1. **Ansible:**
   - Ansible must be installed on the control machine from which you plan to run the playbook. If Ansible is not installed, you can install it using this [link](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

2. **SSH Access to Target Servers:**
   - Ensure that you have SSH access to the target servers where Jenkins will be installed.

4. **Jenkins Repository Key URL:**
   - You will need the URL of the Jenkins repository key. Specify the URL when running the playbook by setting the `jenkins_repo_key_url` variable in the variables folder.

5. **Jenkins Repository URL:**
   - You will also need the URL of the Jenkins APT repository. Specify the URL when running the playbook by setting the `jenkins_repo_url` variable.

# Steps 
* Before going further check the link for Ansible Code: 

**Step 1: Dynamic Inventory Setup** 

```yaml
[defaults]

# some basic default values...


# Use AWS EC2 dynamic inventory for managing hosts
inventory      = aws_ec2.yml

# Disable SSH host key checking for convenience.
host_key_checking = False

# Specify the path to the private key file for SSH connections.
private_key_file = /home/ubuntu/vd.pem

Sets the remote user for SSH connections to 'ubuntu'
remote_user = ubuntu

[inventory]
# enable inventory plugins, default: 'host_list', 'script', 'auto', 'yaml', 'ini', 'toml'
enable_plugins = aws_ec2, host_list, virtualbox, yaml, constructed, script, auto, ini, toml
```

> [!NOTE]
>Ensure that the dynamic inventory script is properly configured with the necessary AWS credentials and filters to fetch the desired hosts.

**Step 2:  AWS EC2 Inventory**

```yaml
---
plugin: aws_ec2
regions:
  - eu-north-1

groups: 
  ubuntu: "'ubuntu' in tags.OS"
```

1. `plugin: aws_ec2`: Specifies the use of the aws_ec2 plugin as the dynamic inventory source. This plugin is designed to fetch information about EC2 instances in AWS.
2. `regions: - eu-north-1`: Indicates the AWS region(s) from which the dynamic inventory should fetch information. In this case, it's set to the eu-north-1 region.
3. `groups`: Defines Ansible groups based on certain criteria. Groups are a way to organize and categorize hosts in the inventory.
4. `ubuntu: "'ubuntu' in tags.OS"`: Creates an Ansible group named ubuntu. This group includes EC2 instances where the tag named OS has a value of 'ubuntu'.

