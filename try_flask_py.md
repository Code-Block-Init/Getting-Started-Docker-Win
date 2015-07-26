***
How to add, configure and run Flask-python in Docker on Ubuntu for Windows?
***
```sh
$ docker run -it --name="<add container name>" ubuntu bash
$ docker top <add container name>
$ apt-get update
$ apt-get install -y python python-pip wget
$ pip install Flask
$ docker commit -m "installed python and flask" <add container name>
$ docker images
$ docker tag <image id> <add container name>
$ docker history <add container name>
$ docker run -it -p 5000:5000 <add container name> bash
$ wget https://raw.githubusercontent.com/odewahn/docker-jumpstart/master/examples/hello.py
$ python hello.py
$ VBoxManage controlvm boot2docker-vm natpf1 "flask-server,tcp,127.0.0.1,5000,,5000"
$ curl localhost:5000
$ docker ps
$ docker kill <image id> ## if wish to delete file
$ docker ps -a
$ docker rm <image id> ## to get rid of ghost container
```
