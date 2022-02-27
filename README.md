# Python-microservice
Deploying a Python microservice using Docker and Kubernetes
# Prerequistes and Assumptions
assuming all tasks are done using an linux based operating system.

1.a Python development environment.

2.a Docker environment running.

3.a Kubernetes cluster running.

4.Have the kubectl command line (kubectl CLI) installed.

# Instructions to Build the application using Dockerfile
Dockerfile file is created according to the python microservice application source code,

to run the dockerfile
cd to the directory containing the Dockerfile
    
    $ docker build -t job1:1.0 .
    
    $ docker build -t job2:1.0 .
    
    $ docker build -t api-route:1.0 .
    
    $ docker images
  you will see the images built
  
To run the image

    $docker run -p  job1
    $docker run -p  job2
    $docker run -p  api-route

# Deploying using Kubernetes
Assuming that the kubernetes cluster is running in the same root directory of the go-app
,The docker Image is pushed to Dockerhub.
deployment.yaml and service.yaml is created

To apply the deployment. (cd to the directory containing the files)
Run the following from the directory


    $kubectl apply -f deployment.yaml

#Loadbalancer service
port, pointing to port 8080
targetPort

To run the Service

    $kubectl apply -f service.yaml

#To run Job1 and Job2 as Cronjob

    $kubectl apply -f cronjob1.yaml
    
    $kubectl apply -f cronjob2.yaml

To check scheduled cronjobs

    $ kubectl get cronjob.
