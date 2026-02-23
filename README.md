# Getting started

This is the Docker Compose React/mySQL App from the Docker documentation starting guide, converted to a Kubernetes deployment and hosted on DigitalOcean cloud.

This repository is a sample application for users following the getting started guide at https://docs.docker.com/get-started/.

The application is based on the application from the getting started tutorial at https://github.com/docker/getting-started

## Kubernetes

### Instructions

Create a Kubernetes cluster on DigitalOcean

Backup the config file for the local Kubernetes of Rancher Desktop located in the .Kube folder in the home directory.

Download the config file for the Kubernetes Cluster from DigitalOcean and replace the existing config file in the .Kube folder

From a terminal in the Kubernetes folder, apply all the deployment yaml to the DigitalOcean cluster using the command:

kubectl apply -f .

Get a list of the Pods created on DigitalOcean:

kubectl get pods -w

Port forward to the DigitalOcean cluster to confirm the deployment:

kubectl port-foward <pod name> 3000:3000

