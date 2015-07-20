```
Getting Started with Docker in Windows
```
<b>Step 1:</b> Starters <br>
-- Git (it must be latest)<br>
-- VirtualBox <br>
If using old version, upgrade to <code>VirtualBox 4.3.30</code> <br>
To check the version,
```sh
$cd /d/VirtualBox/
$virtualbox --version
```
<b>Step 2:</b> Docker installation<br>
Cloning the repo branch
```sh
$ git clone https://github.com/dragonwolverines/Getting-Started-Docker-Win.git --branch docker-1.7.1 --single-branch
```
Open Git.
```sh
$cd /d/docker-1.7.1/
$start.sh
initializing...

starting...

dell@DELL3521 /d/docker1.7.1
$ docker --version
Docker version 1.7.1, build 786b29d

dell@DELL3521 /d/docker1.7.1
$ docker version
Client version: 1.7.1
Client API version: 1.19
Go version (client): go1.4.2
Git commit (client): 786b29d
OS/Arch (client): windows/amd64
```
<b>Step 3:</b> Installing boot2docker<br>
```sh
$boot2docker init
$boot2docker up
```