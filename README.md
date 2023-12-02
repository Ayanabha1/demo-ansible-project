# Demo Ansible Project

Presenting an Ansible project designed to streamline the configuration of your virtual machines, such as AWS EC2 instances, with a single command ( i.e., ```npm run start_vms``` ).

Within each virtual machine, a Docker container will be deployed to execute a Node.js application on port 8000. Additionally, an Nginx reverse proxy will be set up to forward any incoming requests on port 80 to port 8000. 

## Configuration Flow 

Flow of Ansible to configure the vms is as follows:

- Install and setup docker
- Clone Github Repository
- Start docker container ```docker-compose up```
- Install Nginx
- Configure Nginx on the virtual machines with a custom configuration, enabling it to act as a reverse proxy forwarding requests from port 80 to port 8000.

## High Level Design (HLD)
![image](https://github.com/Ayanabha1/demo-ansible-project/assets/63809278/9ae6208c-6e06-423a-aab0-7938f39c1f25)

## Usage Instructions

- Copy the [ansible](https://github.com/Ayanabha1/demo-ansible-project/tree/master/ansible) folder to the root directory of your project

- Create an inventory file named ```inventory```, following the format outlined in the [inventory_example](https://github.com/Ayanabha1/demo-ansible-project/blob/master/ansible/inventory_example)

- Populate the inventory file with the IP addresses of your virtual machines.

- Execute the command ```npm run start_vms```.

- Sit back, relax, and enjoy a cup of coffee while Ansible takes care of the configuration process. ☕

