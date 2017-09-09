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
$ docker run -d -p 9999:80 -v $(pwd):/var/app --name my_app helloworld
```
Replace `my_app` with desired name of your container.  

Open `http://localhost:9999` in the browser.  

## Creating a project:  
* run composer install
```
docker exec -it my_app sh
cd /var/app
php7 /usr/sbin/composer install --prefer-dist -o --working-dir=/var/app
```
* create Lumen project
```
./vendor/bin/lumen new my_awesome_lumen_app
ln -s my_awesome_lumen_app/public/ public
php7 /usr/sbin/composer install --prefer-dist -o --working-dir=/var/app/my_awesome_lumen_app
```

## Using

Go inside the container
```
$ docker exec -it my_app sh
```


## TODO:  
* composer install doesn't create vendor dir
* make lumen global
