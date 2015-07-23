```sh
$cd /d/docker1.7.1
$boot2docker up
$export DOCKER_HOST=tcp://192.168.59.103:2376
$export DOCKER_CERT_PATH='C:\Users\dell\.boot2docker\certs\boot2docker-vm'
$export DOCKER_TLS_VERIFY=1
$mkdir try-docker && cd try-docker
$touch Dockerfile
```
```sh
##
## Type:
FROM docker/hello-world:latest
## and save it to Dockerfile
##
```
```sh
# docker-cow.sh
##
## Docker Cow
##
$the_cow <<EOC

                    ##         .
              ## ## ##        ==
           ## ## ## ## ##    ===
       /"""""""""""""""""\___/ ===
  ~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~
       \______ o           __/
         \    \         __/
          \____\_______/
EOC

# credits
# https://github.com/moxiegirl/whalesay
```
```sh
# Editing and adding some more lines in "Dockerfile"
FROM docker/hello-world:latest

RUN apt-get -y update && apt-get install -y docker-cow

CMD /d/docker1.7.1/try-docker/docker-cow -a
```
```sh
$docker build try-docker
# the build will fail due to docker/hello-world, "but the steps are correct only". This was my 1st attempt.
```
```sh
# For good experience, try this test sample: https://github.com/ashumeow/tutorials/blob/master/docs/windows/step_four.md
dell@DELL3521 /d/docker1.7.1
$ mkdir test && cd test

dell@DELL3521 /d/docker1.7.1/test
$ touch Dockerfile

dell@DELL3521 /d/docker1.7.1/test
$ notepad Dockerfile&
[1] 6524

dell@DELL3521 /d/docker1.7.1/test
$ cd /d/docker1.7.1

dell@DELL3521 /d/docker1.7.1
$ docker build -t test
docker: "build" requires 1 argument.
See 'd:\docker1.7.1\docker.exe build --help'.

Usage: docker build [OPTIONS] PATH | URL | -

Build a new image from the source code at PATH

dell@DELL3521 /d/docker1.7.1
$ docker build test
SECURITY WARNING: You are building a Docker image from Windows against a Linux D
ocker host. All files and directories added to build context will have '-rwxr-xr
-x' permissions. It is recommended to double check and reset permissions for sen
sitive files and directories.
Sending build context to Docker daemon 2.048 kB
Sending build context to Docker daemon
Step 0 : FROM docker/whalesay:latest
 ---> fb434121fc77
Step 1 : RUN apt-get -y update && apt-get install -y fortunes
 ---> Running in 4ebccefae57e
Ign http://archive.ubuntu.com trusty InRelease
Ign http://archive.ubuntu.com trusty-updates InRelease
Ign http://archive.ubuntu.com trusty-security InRelease
Hit http://archive.ubuntu.com trusty Release.gpg
Get:1 http://archive.ubuntu.com trusty-updates Release.gpg [933 B]
Get:2 http://archive.ubuntu.com trusty-security Release.gpg [933 B]
Hit http://archive.ubuntu.com trusty Release
Get:3 http://archive.ubuntu.com trusty-updates Release [63.5 kB]
Get:4 http://archive.ubuntu.com trusty-security Release [63.5 kB]
Hit http://archive.ubuntu.com trusty/main Sources
Hit http://archive.ubuntu.com trusty/restricted Sources
Hit http://archive.ubuntu.com trusty/universe Sources
Hit http://archive.ubuntu.com trusty/main amd64 Packages
Hit http://archive.ubuntu.com trusty/restricted amd64 Packages
Hit http://archive.ubuntu.com trusty/universe amd64 Packages
Get:5 http://archive.ubuntu.com trusty-updates/main Sources [272 kB]
Get:6 http://archive.ubuntu.com trusty-updates/restricted Sources [3158 B]
Get:7 http://archive.ubuntu.com trusty-updates/universe Sources [157 kB]
Get:8 http://archive.ubuntu.com trusty-updates/main amd64 Packages [728 kB]
Get:9 http://archive.ubuntu.com trusty-updates/restricted amd64 Packages [18.1 k
B]
Get:10 http://archive.ubuntu.com trusty-updates/universe amd64 Packages [387 kB]

Get:11 http://archive.ubuntu.com trusty-security/main Sources [111 kB]
Get:12 http://archive.ubuntu.com trusty-security/restricted Sources [1874 B]
Get:13 http://archive.ubuntu.com trusty-security/universe Sources [32.0 kB]
Get:14 http://archive.ubuntu.com trusty-security/main amd64 Packages [396 kB]
Get:15 http://archive.ubuntu.com trusty-security/restricted amd64 Packages [14.8
 kB]
Get:16 http://archive.ubuntu.com trusty-security/universe amd64 Packages [143 kB
]
Fetched 2392 kB in 27s (85.5 kB/s)
Reading package lists...
Reading package lists...
Building dependency tree...
Reading state information...
The following extra packages will be installed:
  fortune-mod fortunes-min librecode0
Suggested packages:
  x11-utils bsdmainutils
The following NEW packages will be installed:
  fortune-mod fortunes fortunes-min librecode0
0 upgraded, 4 newly installed, 0 to remove and 25 not upgraded.
Need to get 1961 kB of archives.
After this operation, 4817 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu/ trusty/main librecode0 amd64 3.6-21 [771
 kB]
Get:2 http://archive.ubuntu.com/ubuntu/ trusty/universe fortune-mod amd64 1:1.99
.1-7 [39.5 kB]
Get:3 http://archive.ubuntu.com/ubuntu/ trusty/universe fortunes-min all 1:1.99.
1-7 [61.8 kB]
Get:4 http://archive.ubuntu.com/ubuntu/ trusty/universe fortunes all 1:1.99.1-7
[1089 kB]
debconf: unable to initialize frontend: Dialog
debconf: (TERM is not set, so the dialog frontend is not usable.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (This frontend requires a controlling tty.)
debconf: falling back to frontend: Teletype
dpkg-preconfigure: unable to re-open stdin:
Fetched 1961 kB in 15s (129 kB/s)
Selecting previously unselected package librecode0:amd64.
(Reading database ... 13116 files and directories currently installed.)
Preparing to unpack .../librecode0_3.6-21_amd64.deb ...
Unpacking librecode0:amd64 (3.6-21) ...
Selecting previously unselected package fortune-mod.
Preparing to unpack .../fortune-mod_1%3a1.99.1-7_amd64.deb ...
Unpacking fortune-mod (1:1.99.1-7) ...
Selecting previously unselected package fortunes-min.
Preparing to unpack .../fortunes-min_1%3a1.99.1-7_all.deb ...
Unpacking fortunes-min (1:1.99.1-7) ...
Selecting previously unselected package fortunes.
Preparing to unpack .../fortunes_1%3a1.99.1-7_all.deb ...
Unpacking fortunes (1:1.99.1-7) ...
Setting up librecode0:amd64 (3.6-21) ...
Setting up fortune-mod (1:1.99.1-7) ...
Setting up fortunes-min (1:1.99.1-7) ...
Setting up fortunes (1:1.99.1-7) ...
Processing triggers for libc-bin (2.19-0ubuntu6.6) ...
 ---> f54ada5fd538
Removing intermediate container 4ebccefae57e
Step 2 : CMD /d/docker1.7.1/test/ -a | cowsay
 ---> Running in d1174a464993
 ---> 22beccfa8d38
Removing intermediate container d1174a464993
Successfully built 22beccfa8d38
```
