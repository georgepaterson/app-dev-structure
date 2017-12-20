# Application development structure

This document will walk through the structure of basic Web application.

## Client

### Version control

### Unit tests

## Server

### Version control

### Unit tests

## Data

### Database schema

### Version control

### Unit tests

## Cloud hosting

## Deployment

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