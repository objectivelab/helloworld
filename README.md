# helloworld

Simple easy to setup PHP application, can be used for testing or creation a new PHP project


## Prerequisites

* Git
* Docker

## Installation

Clone repository
```
$ git clone https://github.com/objectivelab/helloworld.git
```

Build and run container
```
$ docker build . -t helloworld
$ docker run -d -p 9999:80 -v $(pwd):/var/app --name helloworld_app helloworld
```
Replace `helloworld_app` with desired name of your container.  

Open `http://localhost:9999` in the browser.  

## Using

Go inside the container
```
sudo docker exec -it 8af4b1d3468d sh
```