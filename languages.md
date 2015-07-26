```sh
## Downloading languages for Docker in Ubuntu 14.04 (VM) for Windows
$ cd /d/docker1.7.1
$ boot2docker up
$ export DOCKER_HOST=tcp://192.168.59.103:2376
$ export DOCKER_CERT_PATH='C:\Users\dell\.boot2docker\certs\boot2docker-vm'
$ export DOCKER_TLS_VERIFY=1

## opening Ubuntu bash
$ docker run -it ubuntu bash

## For python
$ apt-get update
$ apt-get install -y python python-pip wget
$ python --version

## For Ruby
$ apt-get install ruby-full

## For Java
$ sudo apt-get install default-jre

## For nodeJS
$ sudo apt-get install nodejs
$ sudo apt-get install npm

## For Go
$ sudo apt-get install python-software-properties
$ sudo add-apt-repository ppa:duh/golang
$ sudo apt-get update
$ sudo apt-get install golang

## For R
$ sudo apt-get install r-base r-base-dev

## For Erlang
$ sudo apt-get install erlang erlang-doc

## For PHP
$ sudo add-apt-repository ppa:eugenesan/ppa
$ sudo apt-get update
$ sudo apt-get install php5

## For Rust
# $ curl -sSf https://static.rust-lang.org/rustup.sh | sh

## For Haskell
$ sudo add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) universe"
$ sudo apt-get update
$ sudo apt-get install haskell-platform

For C/C++
$ sudo apt-get install g++
```
