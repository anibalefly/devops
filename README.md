[![<ORG_NAME>](https://circleci.com/gh/anibalefly/devops.svg?style=shield)](<LINK>)

## Project Overview

A complete README file should include:

A summary of the project
Instructions on how to run the Python scripts and web app (simply listing command line calls will suffice), and
A short explanation of the files in the repository.
The README should also include the "passed" status badge (shown above) at the top of the README.

This application serves out predictions (inference) about housing prices through API calls via a machine-learning microservice API.

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Key Files

* app.py - the main Python application implementing the microservice API
* ./run_docker.sh - builds the app.py application into a container and runs it
* ./upload_docker.sh - pushes the application into the docker registry so it can run on Kubernetes
* ./run_kubernetes.sh - runs the application in Kubernetes (must run upload_docker.sh first)
* ./make_prediction.sh - tests the application by sending some sample data to the application

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Sample output

Sample output files are provided in the output_txt_files directory for both Docker and Kubernetes

