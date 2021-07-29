# Steps to dockeraize a Flask app

docker build -f Dockerfile -t docker_ktw .

### To build without cache (takes longer time)
docker build -f Dockerfile --no-cache -t docker_ktw .


### To go inside the docker container & run bash
	
docker run -ti docker_ktw /bin/bash

### Below command activate a python virtual environment and run Flask app with Docker's port exposed to 7000

docker run -d -p 7000:5000 -ti docker_ktw /bin/bash -c "cd src/ && source activate mlenv && python app.py"
