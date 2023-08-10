##Docker Installation Guide in Ubuntu
This is guide provide step by step instruction for installing Docker in Ubuntu.

![image](https://1000logos.net/wp-content/uploads/2021/11/Docker-Logo-2013-500x281.png)

###Prerequisites
Before begin , ensure that you have the following
1.Ubuntu installed on your machine 
2.Check for gnome-terminal if not their install it using this command
```shell
sudo apt install gnome-terminal
```
3.Uninstall the tech preview or beta version of Docker Desktop for ubuntu
```shell


sudo apt remove docker-desktop
```

```shell
rm -r $HOME/.docker/desktop
sudo rm /usr/local/bin/com.docker.cli
sudo apt purge docker-desktop
```
###Install using the apt repository
`*`The apt package manager requires a few prerequisite packages on the system to use packages over HTTPS. Run the following command to allow Ubuntu to access the Docker repositories over HTTPS:
```shell
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
```
 `*`Add GPG key to apt repository
A GPG key verifies the authenticity of a software package. Add the Docker repository GPG key to your system by running:
```shell
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

`*`Run the following command to add the Docker repository to apt sources:
```shell
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
Adding the Docker official repository to the apt package manager.
![image](https://phoenixnap.com/kb/wp-content/uploads/2022/10/add-docker-official-repository-to-apt.png)
 Add Docker Repository

```
###Install Docker Engine

   1. Update the apt package index:
```shell
 sudo apt-get update
```
2.Install Docker Engine, containerd, and Docker Compose.

```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
3.Verify that the Docker Engine installation is successful by running the hello-world image.
```shell
sudo docker run hello-world
```
###Download latest DEB package
use this link to download the package
[DEB package](https://docs.docker.com/desktop/install/ubuntu/)

![image](https://phoenixnap.com/kb/wp-content/uploads/2022/10/create-a-test-container-with-docker.png)
run this commands to docker destop to system
in version write version you downloaded and arch write archived file name.
```shell
sudo apt-get update
sudo apt-get install ./docker-desktop-<version>-<arch>.deb
```
open a docker icon on the system

![image](https://res.cloudinary.com/practicaldev/image/fetch/s--eUI8XeV6--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/49x491yt6f2esenrd4er.png)


[def]: https://docs.docker.com/desktop/install/ubuntu/