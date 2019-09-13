# Deployment of MediaWiki on docker using ansible.
Assignment

# Installs MediaWiki and MySQL containers on CentOS 7 servers.

# Requirements:
IP of the remote host with CentOS 7 installed is required to pass for "inv_hosts" variable, where it is required to setup.

# To run the playbook:
Edit the ansible/hosts inventory file to include the names or URLs of the servers you want to deploy.

# Run the playbook using:
ansible-playbook -i /ansible/hosts ansible/mediawiki.yml -e "inv_hosts=<IP/Group>"

# Description
- This playbook will check the passed IP and will call the role mw-docker-setup, which has dependency on docker, so it will call the docker role and setup the pre requiesites for it. 
- Once docker is successfully setup, it will copy the respective files in that host and use docker compose to complete the setup
