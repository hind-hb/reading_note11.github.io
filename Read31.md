# Read 31: Django REST Framework & Docker:

## A Beginner's Guide to Docker

* With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore.

* The entire development environment is isolated: programming language, software packages, databases, and more.

*  Docker is a complex beast under the hood.

* **Linux Containers**: Docker is really just Linux containers which are a type of virtualization.

* **Containers vs Virtual Environments**: 
  
  * Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. 
  * Virtual environments can only isolate Python packages.
  * Also we can’t run a production database or other services within virtual environments.

* **Install Docker**:

  * To install Docker we need to download the desktop app on our computer and create a free account.
  * It should be at least version 19.
```
            $ docker --version
          Docker version 19.03.5, build 633a0ea
```
 
* on Linux, by running the command `sudo pip install docker-compose`. 
  * The version should be at least 1.24.x.
```
          $ docker-compose --version
          docker-compose version 1.24.1, build 4667896b
```

* **Hello, World**: To confirm Docker installed correctly we can run our first command docker run hello-world.  

* **Images and Containers**:
  
  * Images and containers are the two fundamental concepts to grasp when you start with Docker.
  * An image is a snapshot in time of what a project contains.
  * A container is a running instance of the image.

* **Conclusion**:
    
  * Docker is a way to run Linux containers
  * Containers are a lightweight alternative to Virtual Machines
  * Dockerfile is a list of instructions for creating an image
  * Images are made up of one or more layers
  * Containers are a running instance of an image
  * docker-compose.yml controls how to run the container
  * Containers are stateless and ephemeral in nature. We can link the local filesystem via volumes but things become more complex with databases

----

## Library Website and API:

  * Django REST Framework works alongside the Django web framework to create web APIs. 
  
  * The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.
