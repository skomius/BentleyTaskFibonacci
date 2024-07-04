
# Azure function in container

This is single endpoint and probbably will not be used continuously so its endpoint will be deployed to htttp triggered azure function in container. 

# Running locally

- install docker desktop latest version
- build docker image 
- run docker image

# CI/CD 

For CI/CD are used github actions. Pipeline code can be found workflow folder and infrastructure as a code in Iac folder. The main steps:
- Build and push container image to docker hub
- Deploy resources to azure cloud using arm templates
- Run azure function with latest image

 
# Logging

For logging are used azure application insight. It is included in azure ARM deployment script in Iac folder.

# Scalling

Azure functions in contaner can be scaled up to 1000 instaces as long as there's enough cores quota available. Is event driven and scale out automatically, even during periods of high load. Azure Functions infrastructure scales CPU and memory resources by adding more instances of the Functions host, based on the number of events that its functions are triggered. 
