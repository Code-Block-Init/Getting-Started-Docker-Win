```
Getting Started with Docker in Windows
```
<b>Step 1:</b> <b>Pre-requistes</b> <br>
-- Git (it must be latest)<br>
-- VirtualBox <br>
If using old version, upgrade to <code>VirtualBox 4.3.30</code> <br>
To check the version,
```sh
$cd /d/VirtualBox/
$virtualbox --version
```
<b>Step 2:</b> <b>Docker installation</b><br>
Cloning the repo branch
```sh
$ git clone https://github.com/dragonwolverines/Getting-Started-Docker-Win.git --branch docker-1.7.1 --single-branch
```
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
<b>Step 3:</b> <b>Installing boot2docker</b><br>
```sh
$boot2docker init
Generating public/private rsa key pair.
Your identification has been saved in C:\Users\dell\.ssh\id_boot2docker.
Your public key has been saved in C:\Users\dell\.ssh\id_boot2docker.pub.

Initialization of virtual machine "boot2docker-vm" complete.
```
```sh
$boot2docker up
Waiting for VM and Docker daemon to start...
.................................................ooooooooooooooooooooooooooooooo
oooooooooo
Started.
Writing C:\Users\dell\.boot2docker\certs\boot2docker-vm\ca.pem
Writing C:\Users\dell\.boot2docker\certs\boot2docker-vm\cert.pem
Writing C:\Users\dell\.boot2docker\certs\boot2docker-vm\key.pem

To connect the Docker client to the Docker daemon, please set:
    export DOCKER_HOST=tcp://192.168.59.103:2376
    export DOCKER_CERT_PATH='C:\Users\dell\.boot2docker\certs\boot2docker-vm'
    export DOCKER_TLS_VERIFY=1

Or run: `eval "$(boot2docker shellinit)"`
```
<b>Step 4:</b>
```sh
dell@DELL3521 /d/docker1.7.1
$ export DOCKER_HOST=tcp://192.168.59.103:2376

dell@DELL3521 /d/docker1.7.1
$ export DOCKER_HOST=tcp://$(boot2docker ip 2>/dev/null):2376

dell@DELL3521 /d/docker1.7.1
$ export DOCKER_CERT_PATH='C:\Users\dell\.boot2docker\certs\boot2docker-vm'

dell@DELL3521 /d/docker1.7.1
$ export DOCKER_TLS_VERIFY=1
```
```
```
<b>Related Links:</b><br>
[1] <a href="https://docs.docker.com/installation/windows/">Docker for Windows - Official</a><br>
[2] <a href="http://odewahn.github.io/docker-jumpstart">Docker Jumpstart</a><br>
[3] <a href="https://github.com/boot2docker/windows-installer">Docker for Windows - Github</a><br>