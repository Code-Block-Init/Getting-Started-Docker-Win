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
```
