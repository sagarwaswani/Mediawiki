# Deployment of MediaWiki on docker using ansible.
Assignment

# Installs MediaWiki and MySQL containers on CentOS 7 servers.

# Requirements:
IP of the remote host is required to pass for "inv_hosts" variable, where it is required to setup.

# To run the playbook:
Edit the ansible/hosts inventory file to include the names or URLs of the servers you want to deploy.

# Run the playbook using:
ansible-playbook -i /ansible/hosts ansible/mediawiki.yml -e "inv_hosts=<IP/Group>"
