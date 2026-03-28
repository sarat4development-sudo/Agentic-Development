# Week 1

## Goal

Refresh AWS knowledge and get a head start with AI-driven development.

## Project

Create infrastructure to deploy the web application: [scholar-path-web-ui](https://github.com/sarat4development-sudo/scholar-path-web-ui).

### Setup local Cursor

- Install Cursor locally.
- Create a Cursor account and sign up for the free tier.

### Use Cursor for the rest of the work

Use the Cursor chat interface to complete the rest of the setup and infrastructure creation. You can ask Cursor to generate Terraform code for the infrastructure described below and use that code to create the infrastructure.

### GitHub setup

- Create a GitHub account.
- Download (clone) the repository linked above for building the Docker image.
- Create infrastructure scripts in the same repository.

### AWS setup

- An account is already created and you should have an invitation. Account number: **914319167644**.
- Complete your account setup and log in to the AWS console.
- Set up your local environment to connect to AWS using the AWS CLI.

### Infrastructure (Terraform)

Set up infrastructure to host this application:

- Create Docker configuration for the application.
- Create a Kubernetes cluster to host the application.
- Create a load balancer to route traffic to the application.
- Create a Route 53 record that points to the load balancer.

Perform all of this using **Terraform**.

### Stretch goals

- Create a GitHub Actions–based CI/CD pipeline for the application.
- Create environment configurations and a way to deploy those configurations and make them available to the cluster.
