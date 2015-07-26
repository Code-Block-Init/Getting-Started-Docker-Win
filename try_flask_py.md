***
commands
***
```sh
$ docker run -it --name="try_flask" ubuntu bash
$ docker top try_flask
$ apt-get update
$ apt-get install -y python python-pip wget
$ pip install Flask
$ docker commit -m "installed python and flask" try_flask
$ docker images
$ docker tag <image id> simple_flask
$ docker history try_flask
$ docker run -it -p 5000:5000 try_flask bash
$ wget https://raw.githubusercontent.com/odewahn/docker-jumpstart/master/examples/hello.py
$ python hello.py
$ VBoxManage controlvm boot2docker-vm natpf1 "flask-server,tcp,127.0.0.1,5000,,5000"
$ curl localhost:5000
$ docker ps
$ docker kill <image id> ## if wish to delete file
$ docker ps -a
$ docker rm <image id> ## to get rid of ghost container
```
