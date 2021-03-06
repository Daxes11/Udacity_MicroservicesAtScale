[![Daxes11](https://circleci.com/gh/Daxes11/Udacity_MicroservicesAtScale.svg?style=svg)](https://app.circleci.com/pipelines/github/Daxes11/Udacity_MicroservicesAtScale/)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

---

## Files included in this repository

* `app.py` includes our flask app
* `Dockerfile` is needed to build our docker container
* `requirements.txt` contains all dependencies needed for our app
* `run_docker.sh` and `run_kubernetes.sh` can be used to run `app.py` (see below)
* `upload_docker.sh` can be used to upload your Docker container to Docker Hub
* `output_txt_files` has some sample outputs included
* Under `.circleci` you can find the circleci config to test the project 

## Setup the Environment

* Create a virtualenv (`python3 -m venv ~/.devops`) and activate it (`source ~/.devops/bin/activate`)
* Run `make install` to install the necessary dependencies

### Running your flask app `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  First start your minikube cluster with `minikube start` and afterwards `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### Make predictions with `make_predictions.sh`

* After running your flask app use `./make_predictions.sh` to generate a sample query