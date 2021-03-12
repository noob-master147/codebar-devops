# codebar festival 2021 - **Devops Demystified**
_Session by Divyansh Khandelwal_

---
This repository contains the code used in the session with some useful links for the community members.


# Steps to follow along 
<br>

## Step 1 -> Get the Code
Here is the git [repo](https://github.com/noob-master147/codebar-devops)  
Do drop a star, will make me happy 😊

Clone the Repository

```
git clone https://github.com/noob-master147/codebar-devops.git

```
<br>

## Step 2 -> Install Docker and Docker Compose on your system

_Skip this step if you already have installed docker and docker compose._  

> **Docker**  | [Mac](https://docs.docker.com/docker-for-mac/install/)  |  [Windows](https://docs.docker.com/docker-for-windows/install/) | [Ubuntu](https://docs.docker.com/engine/install/ubuntu/) |

> **Docker Compose** [Guide](https://docs.docker.com/compose/install/)

Confirm your installation by running ``sudo docker version`` 
<br><br>

## Step 3 -> Create account on [Docker Hub](https://hub.docker.com/)

<br>

## Step 4 -> Run the project locally
```
sudo docker-compose up --build -d
```

Check the services
```
sudo docker ps
```
![docker ps](./images/dps.png)

| Port | Service |
|:---------|:-------------|
| http://localhost:3000  | React-Frontend |
| localhost:27017 | MongoDB |

<br><br>


## Step 5 -> Create an EC2 instance on AWS
[Read The Docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html)
<br><br>

## Step 6 -> Install Docker and DockerCompose on EC2 instance
Use the script available [here](https://gist.githubusercontent.com/noob-master147/f96aef074bf28d1db7276e365b646ba5/raw/59672002fb99669065e127bc1bc30aa3dca7c8fa/script.sh)

Drop a ⭐ on the [gist](https://gist.github.com/noob-master147/f96aef074bf28d1db7276e365b646ba5) or bookmark it.


* Copy the url _https://gist.githubusercontent.com/noob-master147/f96aef074bf28d1db7276e365b646ba5/raw/66063ad3f8bcefa81ac5c058b1081775462f6aa2/script.sh_

* ```sudo curl https://gist.githubusercontent.com/noob-master147/f96aef074bf28d1db7276e365b646ba5/raw/66063ad3f8bcefa81ac5c058b1081775462f6aa2/script.sh >> script.sh```

* ```sudo bash script.sh``` 
    * After this step you will have docker and docker-compose installed in your EC2 instance. 
<br><br>

## Step 7 -> Copy the Docker-Compose file on EC2 instance
* ```sudo nano docker-compose.yml```
    * paste the docker-compose file contents.
    * press ```ctrl+x y enter``` to save and exit.
<br><br>

## Step 8 -> Pull the images and run
```
sudo docker-compose pull
sudo docker-compose up --build 
```
<br>

## Step 9 -> Setup GitHub Actions for CI/CD pipelines
* add repository secrets
    * HOST
    * PORT
    * USERNAME
    * KEY
    * DOCKER_USER
    * DOCKER_PASSWORD
* Create Workflow YAML file
    * use this [gist](https://gist.github.com/noob-master147/ffa07670434e4696d4a3a29974f30755) as template.
    * update the tags and the image names

<br><br>

## Step 10 -> Push a commit and see the MAGIC !