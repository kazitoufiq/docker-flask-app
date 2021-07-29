# Steps to dockeraize a Flask app

docker build -f Dockerfile -t docker_ktw .

### To build without cache (takes longer time)
docker build -f Dockerfile --no-cache -t docker_ktw .


### To go inside the docker container & run bash
	
docker run -ti docker_ktw /bin/bash

### Below command activate a python virtual environment and run Flask app with Docker's port exposed to 7000

docker run -d -p 7000:5000 -ti docker_ktw /bin/bash -c "cd src/ && source activate mlenv && python app.py"




### Steps to publish in GitHub


## Create a repo in GitHub first AND clone to local machine

## Pre-requisite 
	- ssh-keygen -t rsa 
	- cat /c/Users/kwadud/.ssh/id_rsa.pub 
	- Copy and paste the key at SSH key part in GitHub setting

### 
git clone git@github.com:kazitoufiq/docker-flask-app.git

git status

git add *

git status

git commit -m "changes made"

git config --global user.name "Kazi Toufiq Wadud"

git config --global user.email kazitoufiq@gmail.com

git commit --amend --reset-author

git branch -M main

git push


