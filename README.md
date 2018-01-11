# Application development structure

This document will walk through the structure of basic Web application.

## Client

The client is the point of interaction for the user or customer with the application. The Web client is the fundamental interface for the majority of application; however mobile clients and voice interfaces are a significant method of interacting with applications.

### Web client

Web browser

### Mobile client

Mobile apps
AR/VR

### Voice interface

Alexa
Siri
Google

### Version control

### Unit tests

Authentication

## Server

### Version control

### Unit tests

Service architecture
Authentication

## Data

### Version control

### Database schema

### Unit tests

Business rules
Migration

### Backup

## Cloud hosting

## Deployment

Git is used as the repository. Gitflow workflow is used to create a master and develop branch; features are branched from the develop branch.
All feature code has automated unit tests. Tests are based on TDD or BDD strategies. Jest/Enzyme for React.
Mutation testing is used to test unit tests. Stryker and PIT are examples.
Features have automated functional tests developed. This may include Selenium and API testing.
Automated security testing can be achieved through Zed Attack Proxy, Nessus, BDD security.
Docker is used as a container for development.
An Ansible playbook to automate Docker tooling.
A continuous integration server, typically Jenkins, to automate the build process and deployment.

A typical pipeline will include:

* Checkout code from Git.
* Build Docker image with docker file and Ansible.
* Copy code into image.
* Run build processes.
* Run unit tests.
* Run mutantion tests.
* Run functional tests.
* Push image to registry.
* Deploy to staging cluster.
* Run staging tests.
* Deploy to production cluster.
* Run production tests.
* Switch router to new deployment.
* Stop previous release.

Blue-green deployment is used to maintain uptime. New releases are deployed to the blue environment. Green is the current live environment. If the new release passes production tests, the router is updated to make the new release the green environment. The previous release becomes the blue environment ready for the next release. If there is a problem with the current green environment, it can be switched to the previous release blue environment.

## Penetration Testing

* Playbooks for against tests should be created; these will simply outline what to do to secure the application and it's infrastructure against a test.
* A Red Team will trigger a test and attempt to exploit the test. The Blue Team will respond.

### Denial of Service (DoS) Attack Playbook



 

 



