# How to Install Docker Engine on Ubuntu

**Before install Docker Engine, you need to check and uninstall any conflicting packages.**

run this bellow command

`for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done`

Before install Docker Engine for the first time on a new host machine, need to set up the Docker apt repository then install and update Docker from the repository.
### Add Docker's official GPG key:

`sudo apt-get update`

`sudo apt-get install ca-certificates curl`

`sudo install -m 0755 -d /etc/apt/keyrings`

`sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc`

`sudo chmod a+r /etc/apt/keyrings/docker.asc`


### Add the repository to Apt sources:

`echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \`

 ` sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

`sudo apt-get update`


**To install the latest version, run:**

`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

**Verify that the installation**

`docker version` or `docker --version`

Verify that the installation is successful by running the **hello-world image:**

`sudo docker run hello-world`


Visit docker official sites.

[Install docker from docker official](https://docs.docker.com/engine/install/)

