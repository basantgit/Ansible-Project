# Ansible
Question
1. Which languge use ansible
Ans - Python
2. Is ansible push/pull mechanism
Ans - Push
3. Ansible uses YAML because it is very easy for humans to understand, read and write when compared to other data formats like XML and JSON. Every YAML file
4. What are the features of Ansible?
It has the following features:

Agentless – Unlike puppet or chef there is no software or agent managing the nodes.

Python – Built on top of python which is very easy to learn and write scripts and one of the robust programming languages.

SSH – Passwordless network authentication which makes it more secure and easy to set up.

Push architecture – The core concept is to push multiple small codes to the configure and run the action on client nodes.

Setup – This is very easy to set up with a very low learning curve and any open source so that anyone can get hands-on.

Manage Inventory – Machines’ addresses are stored in a simple text format and we can add different sources of truth to pull the list using plugins such as Openstack, Rackspace, etc.

Password less auth - ssh-copy-id -f "-o identityFile .pem"  ubuntu@54.210.244.136

1. Ensure the six library is installed
The error message suggests that the six module isn't found. You can install the six package using the following command:

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
2. Verify Ansible is using Python 3
It appears from the error output that Ansible might be using Python 3, so you should ensure that Python 3 is correctly configured and the necessary modules are installed. You can verify the Python version being used by Ansible with the following command:

bash
Copy
ansible --version
Make sure that the Python interpreter points to Python 3 (e.g., /usr/bin/python3).

3. Upgrade Ansible
Older versions of Ansible may still have dependencies on Python 2. If you have an outdated version of Ansible, you may want to upgrade it to the latest version to improve compatibility with Python 3. You can upgrade Ansible via pip:

bash
Copy
pip install --upgrade ansible
4. Check the ansible.cfg Configuration
If Ansible is using the wrong Python interpreter, you may want to explicitly set the interpreter to Python 3 in your ansible.cfg file. In the [defaults] section of the ansible.cfg file, add:

ini
Copy
[defaults]
interpreter_python = /usr/bin/python3
