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
<b>Step 4:</b> <b>Getting things ready</b>
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
<b>Step 5:</b> <b>Running for first time</b>
```sh
dell@DELL3521 /d/docker1.7.1
$ docker run hello-world
Post http://192.168.59.103:2376/v1.19/containers/create: malformed HTTP response
 "\x15\x03\x01\x00\x02\x02\x16". Are you trying to connect to a TLS-enabled daem
on without TLS?

dell@DELL3521 /d/docker1.7.1
91c95931e552: Already exists
hello-world:latest: The image you are pulling has been verified. Important: imag
e verification is a tech preview feature and should not be relied on to provide
security.552: Extracting     32 B/32 B
a8219747be10: Extracting    596 B/596 B
Digest: sha256:aa03e5d0d5553b4c3473e89c8619cf79df368babd18681cf5daeb82aab55838d
Status: Downloaded newer image for hello-world:latest
Hello from Docker.fying Checksum
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (Assuming it was not already locally available.)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal. fs layer

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

For more examples and ideas, visit:
 http://docs.docker.com/userguide/
```
<b>Step 6:</b> <b>Getting inside...</b>
```sh
dell@DELL3521 /d/docker1.7.1
$ docker run -it ubuntu bash
root@c28a7a59798d:/# ls
bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
boot  etc  lib   media  opt  root  sbin  sys  usr
root@c28a7a59798d:/# lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 14.04.2 LTS
Release:        14.04
Codename:       trusty
root@c28a7a59798d:/# echo "Meow Meow"
Meow Meow
```
<b>Related Links:</b><br>
[1] <a href="https://docs.docker.com/installation/windows/">Docker for Windows - Official</a><br>
[2] <a href="http://odewahn.github.io/docker-jumpstart">Docker Jumpstart</a><br>
[3] <a href="https://github.com/boot2docker/windows-installer">Docker for Windows - Github</a><br>
