# Project-1 GitHub-Fundamentals - Cloud Security 
 Cloud Security - VMs setup including ELK
Configuring an ELK Server
Lectures cover the following:
* Give an overview of the ELK stack and how it performs network security monitoring. This overview will also give you valuable context for why you're configuring and deploying these tools during the week.
* Provide the project overview as well as suggested milestones for each day.
* Due to Azure Free account limitations, you can only utilize 4vCPUs per region in Azure. Therefore, we will need to create a new vNet in another region for our ELK server.
* By the end of the project, we will have an ELK server deployed and receiving logs from all three web VMs created in the previous cloud weeks.
Activities involve the following:
* Create a new vNet in Azure in a different region, within the same resource group.
* Create a peer-to-peer network connection between your vNets.
* Create a new VM in the new vNet that has 2vCPUs and a minimum of 4GiB of memory.
* Add the new VM to Ansible’s hosts file in your provisioner VM.
* Create an Ansible playbook that installs Docker and configures an ELK container.
* Run the playbook to launch the container.
* Restrict access to the ELK VM.


ELK VM






Filebeat
Lectures cover the following
* Provide a brief overview of Filebeat.
Activities involve the following:
* Navigate to the ELK server’s GUI to view Filebeat installation instructions.
* Create a Filebeat configuration file.
* Create an Ansible playbook that copies this configuration file to the DVWA VMs and then installs Filebeat.
* Run the playbook to install Filebeat.
* Confirm that the ELK Stack is receiving logs.
* Use the same method to install Metricbeat.


Installing Filebeat on the DVWA Container
1. First, make sure that the ELK server container is up and running:
o Navigate to http: 20.53.238.207:5601/app/kibana. Use the public IP address of the ELK server that you created.
o Click 'Explore on my Own'
o If you do not see the Kibana server landing page, open a terminal on your computer and SSH into the ELK server.
* Run docker container list -a to verify that the container is on.
* If it isn't, run sudo docker start elk.
2. Use the ELK server's GUI to begin installing Filebeat on your DVWA VM.
o Navigate to your ELK server's IP address:
* Click Add Log Data.
* Choose System Logs.
* Click on the DEB tab under Getting Started.
o 









