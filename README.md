# containerd_papermc_service
My pipeline of deploying a vanilla minecraft server for my friends. This is a learning project.

Under .github/workflows/ you can find the following github actions workflow files:

## main.yml
* provides the deployment of the S3-hosted SPA frontend user interface
* provides the deployment of the lambda function that serves as backend 
* user interface provides parameters for tailored server hosting service

## deploy-server.yml

* is triggered when form is sent from the SPA frontend UI
* provisions EC2 instance to run the server container
* uses open source CNCF-graduated container runtime 'Containerd' https://containerd.io/
* uses custom Alpine Linux based image for better resource usage
