# Ansible Overview

## 1. **Which language does Ansible use?**

**Ans**: Python

## 2. **Is Ansible push/pull mechanism?**

**Ans**: Push

## 3. **Why does Ansible use YAML?**

Ansible uses YAML because it is very easy for humans to understand, read, and write when compared to other data formats like XML and JSON. Every YAML file in Ansible defines the configuration and tasks to be executed.

## 4. **Features of Ansible**

Ansible has the following features:
- **Agentless**: Unlike Puppet or Chef, there is no software or agent managing the nodes.
- **Python**: Built on top of Python, which is easy to learn and write scripts, and is one of the most robust programming languages.
- **SSH**: Passwordless network authentication, making it more secure and easy to set up.
- **Push Architecture**: The core concept is to push multiple small codes to configure and run actions on client nodes.
- **Setup**: Easy to set up with a low learning curve and open-source, allowing anyone to get hands-on.
- **Manage Inventory**: Machines' addresses are stored in a simple text format, and we can add different sources of truth to pull the list using plugins like Openstack, Rackspace, etc.
  
## 5. **Passwordless Authentication**

To set up passwordless SSH authentication, use the following command:

```bash
ssh-copy-id -f "-o identityFile .pem" ubuntu@54.210.244.136
6. Ensure the six library is installed
The error message suggests that the six module isn't found. You can install the six package using the following commands:

For Python 3:

bash
Copy
sudo apt-get update
sudo apt-get install python3-six
For Python 2:

bash
Copy
sudo apt-get install python-six
Alternatively, you can install it using pip:

bash
Copy
pip install six
7. Verify Ansible is using Python 3
It appears from the error output that Ansible might be using Python 3. To ensure that Python 3 is correctly configured and the necessary modules are installed, run the following command:

bash
Copy
ansible --version
Make sure that the Python interpreter points to Python 3 (e.g., /usr/bin/python3).

8. Upgrade Ansible
Older versions of Ansible may still have dependencies on Python 2. To upgrade Ansible to the latest version and improve compatibility with Python 3, use the following command:

bash
Copy
pip install --upgrade ansible
9. Check the ansible.cfg Configuration
If Ansible is using the wrong Python interpreter, you can explicitly set the interpreter to Python 3 in the ansible.cfg file. In the [defaults] section of the ansible.cfg file, add the following:

ini
Copy
[defaults]
interpreter_python = /usr/bin/python3
10. Setup EC2 Collection and Authentication
Install boto3
bash
Copy
pip install boto3
Install AWS Collection
bash
Copy
ansible-galaxy collection install amazon.aws
11. Setup Vault
Create a password for the vault:

bash
Copy
openssl rand -base64 2048 > vault.pass
Add your AWS credentials using the following vault command:

bash
Copy
ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass
This Markdown provides an overview of Ansible, its features, installation commands, configuration, and how to work with EC2, AWS, and Vault.

css
Copy

You can directly use this Markdown content for your documentation or as a LinkedIn post! It organizes the content effectively, providing clear sections with code blocks for easier readability.


