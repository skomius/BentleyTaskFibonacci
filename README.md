
Azure function in container

This is single endpoint and probbably will not be used continuously so its endpoint will be deployed to htttp triggered azure function in container. 

Running locally

- install docker desktop latest version
- build docker image 
- run docker image

CI/CD 

For CI/CD are used github actions. Pipeline code can be found workflow folder and infrastructure as a code in Iac folder. The main steps by order:
- Build and push container image to docker hub
- Deploy resources to azure cloud using arm templates
- Daploy image to 

Logging

For logging are used azure application insight. It is included in azure ARM deployment script in Iac folder.

Scalling
