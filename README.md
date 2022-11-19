# devops
Step1 : create a unbutu linux

step2 : login to : ssh durga@20.219.56.0 <paas:devops@123456789>

step3 : apt install virtualbox

step4 : apt install vagrant

step5 : vagrant init

step6 : vagrant up

step7 : sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
Once all the packages have been installed, add the Docker GPG key

$ sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmour -o /etc/apt/trusted.gpg.d/docker.gpg
In the next step, add the official Docker repository to your Ubuntu 22.04 system

$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
Next, update the local package index to make the system, aware of the newly added repository.

$ sudo apt update
Then install Docker from the official Docker repository,

$ sudo apt install docker-ce -y
The command installs Docker alongside additional packages that will be required by Docker to function as expected.

Install-docker-ce-apt-command-ubuntu

Once Docker is installed, add the currently logged-in user to the Docker group to avoid running Docker as a sudo user every time you run Docker.

$ sudo usermod -aG docker ${USER}
$ newgrp docker
Step 3) Verify Docker is running on all the nodes
Once installed, the Docker daemon starts automatically. You can verify that the service is running by running the command:

$ sudo systemctl status docker
Docker-Service-Status-Ubuntu-22-04

Additionally, be sure to enable the Docker service so that it starts automatically on boot time.

$ sudo systemctl enable docker
Step 4) Create Docker Swarm Cluster
The next step is to initialize the Docker Swarm on the Manager node. Once initialized, we will then add the worker nodes to the cluster.


Step8 : docker stack deploy -c docker-stack.yml app
step9 : docker service ls
step10 : curl localhost:5000
