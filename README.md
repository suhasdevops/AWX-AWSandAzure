# AWXandAWS

### Requisites:

# AWS account

# Install Ansible Tower using following Documents URLs:
https://www.linuxtechi.com/install-ansible-awx-docker-compose-centos-8/
https://www.howtoforge.com/tutorial/how-to-install-ansible-awx-with-docker-on-centos/

   OR 

# Directly use vagrantfile in repo and hit the VM's IP for AWX console.

URL: https://localhost
Username: admin
Password: password

Useful docker commands:
- $ docker ps
- $ docker exec -it container_id /bin/bash

Check Installed:
- Ansible
- python
- python-pip
- pip install boto

## Notes:
- create {{ projects }} under var/lib/awx/ in docker container.
- uncomment {{ project_data_dir }} in /opt/awx/installer/inventory file in host machine and restart.

## AWX-Dashboard:
- first create project with manual SCM type ans select playbook folder accordingly
- create job template with default inventory and playbook yml file
- and finally run the job.

:)
