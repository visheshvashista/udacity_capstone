# UdacityMicroservicesProject
Udacity NanoDegree Project 4
Screenshots for various steps have been added to screenshots directory

# commands
# set up virtual environment
python3 -m venv ~/.UdacityMicroservicesProject
source ~/.UdacityMicroservicesProject/bin/activate

# install dependencies
cd UdacityMicroservicesProject
make install

# do linting
make lint

# create docker image 
./run_docker.sh 

# run predictions
./make_predictions.sh

# upload docker image to docker repository
# login to docker
# docker login -u="$DOCKER_USERNAME" -p="$DOCKER_PASSWORD"
./upload_docker.sh

# deploy docker image  to kubernates
# In ubantu image on windows 10 server
# download minikube and kubectl and place run_kubernates.sh and make_runpredictions.sh
sudo servcies docker start 
minikube start
./run_kubernetes.sh
./make_predictions.sh

# stop minikube
minikube stop

# successfuly circleci lint test
https://app.circleci.com/pipelines/github/visheshvashista/UdacityMicroservicesProject/7/workflows/82882f03-d924-4893-8512-58c3c4565dbc

# markdown status 
[![CircleCI](https://circleci.com/gh/visheshvashista/UdacityMicroservicesProject.svg?style=svg&circle-token=33998a4727bca4c58f0acc3ee79293cd8ccc0a88)](https://circleci.com/gh/visheshvashista/UdacityMicroservicesProject.svg?style=svg&circle-token=33998a4727bca4c58f0acc3ee79293cd8ccc0a88)
