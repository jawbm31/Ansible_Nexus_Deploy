Ansible Playbook for Nexus Repository Installation


Overview
This Ansible playbook automates the installation and configuration of Nexus Repository on a webserver. It performs the following tasks:

- Installs Java (OpenJDK 8) and networking tools (net-tools).
- Downloads and extracts the Nexus installer to the /opt/ directory.
- Creates a user and group (nexus) and assigns the appropriate permissions to the Nexus directory.
- Configures Nexus to run as the nexus user.
- Starts Nexus Repository service.
- Verifies the Nexus process is running using ps and netstat.


Installation
1. Clone the Repository
First, clone the repository to your local machine:

bash
Copier
git clone https://github.com/jawbm31/Ansible_Nexus_Deploy.git
cd Ansible_Nexus_Deploy
2. Modify the hosts File
Ensure that your hosts file or Ansible inventory is correctly set up to point to the webserver or target server where you want to install Nexus.

Example:

[webserver]
your.server.ip



3. Run the Playbook
You can now run the playbook using the following command:
- ansible-playbook -i hosts setup-nexus.yml
This will execute the playbook on your webserver.

