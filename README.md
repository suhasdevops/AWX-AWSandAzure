# AWS and Azure provising with AWX

### Requisites:
- AWS account
- Azure account
- AWX machine

## Install Ansible Tower using following Documents URLs:
https://www.linuxtechi.com/install-ansible-awx-docker-compose-centos-8/
https://www.howtoforge.com/tutorial/how-to-install-ansible-awx-with-docker-on-centos/

   OR 

## Directly use vagrantfile in repo and hit the VM's IP for AWX console.

AWX_URL: https://localhost
AWX_Username: admin
AWX_Password: password

Useful docker commands:
- $ docker ps
- $ docker exec -it container_id /bin/bash

Check Installed:
- Ansible
- python
- python-pip
- pip install boto

### Important:
- create {{ projects }} under var/lib/awx/ in docker container awx_web.
- uncomment {{ project_data_dir }} in /opt/awx/installer/inventory file in host machine and restart.
- AWS authentication we have use AccessKeyID, SecretAccessKey of admin user.
- And in Azure we have use SubscriptionID, ClientID, TenantID, ClientSecretKey for authentication. 
  (ClientSecretKey needs to create from App registrations -> Application(client)ID)
  This Azure Ids needs to be configure directly in AWX

### AWX-Dashboard:
- first create project with manual SCM type ans select playbook folder accordingly
- create job template with default inventory and playbook yml file
- and finally run the job.


