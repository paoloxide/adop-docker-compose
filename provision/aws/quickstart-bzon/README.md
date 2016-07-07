### The Accenture DevOps Platform: Overview (bzon extension)

This is an ADOP platform using Gitlab as the Git Repository and Code Review tool. Though Gerrit is still in place when you launch this Stack, it will be hidden from the DevOps Dashboard landing page.

CF-ADOP-SingleNode.json will provide you the following AWS Resources:

1. 1 VPC with 1 Public Subnet.
2. 1 AWS Linux EC2 Instance with Elastic IP.

I recommend you to use this Single EC2 template, because a lot might be change in the swarm clustered templates when docker 1.12 is released.

### The Landing Page
![HomePage](https://raw.githubusercontent.com/bzon/adop-docker-compose/master/img/home-extended.png)

### Cartridge Loader

I'm with @arcyteodoroacn in creating our own platform loader for Gitlab and these are my forked projects from him:

https://github.com/bzon/adop-b-framework-gitlab-load-platform.git

Using this git clone url as the parameter of the original "Load Platform" job in Jenkins will give you a job named "Gitlab Load Platform".

https://github.com/bzon/adop-b-framework-gitlab-platform-management.git

Gitlab Load Platform job should use the above git url as a parameter for it to be able to create the "Generate Workspace" job in Jenkins.
