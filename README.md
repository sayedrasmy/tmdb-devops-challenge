## To run from CMD

In project folder run

npm start

## Build Docker

In project folder run

docker build -t {image name} . 

docker run -p 3000 {image name}  

# Ansible Playbook for Docker and Nginx Setup

This Ansible playbook is designed to set up an environment on a remote server where Docker is installed and running, copy application files from the local machine After you ran pipline to the remote server, build a Docker image, and run an Nginx container to serve the application.

## Prerequisites

- Ansible installed on the local machine.
- Docker installed on the remote server.
- SSH access to the remote server.
- Ansible inventory file configured with the remote server details.

## Inventory File

Create an inventory file `inventory.ini` with the following content, replacing `your_remote_server` with the actual hostname or IP address of your remote server:
## To run ansible individual  
ansible-playbook -i inventory.ini  playbook.yml

## To run ansbile phase from jenkins 
run the pipline at jenkinsfile
