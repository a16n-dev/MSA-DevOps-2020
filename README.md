# MSA-DevOps-2020

## Deployment

[![Build Status](https://dev.azure.com/msa-devops-alexn/msa-devops-project-2020/_apis/build/status/alexn400.MSA-DevOps-2020?branchName=master)](https://dev.azure.com/msa-devops-alexn/msa-devops-project-2020/_build/latest?definitionId=5&branchName=master)

The deployed app can be viewed here:
https://alexn-msa-devops.azurewebsites.net/

# Pipelines

## Build pipeline
My build pipeline consists of the following tasks:

- Checkout branch from github repo
- Install node.js
- Install dependencies for app
- Run the react build script to create a production build
- Archive the build once complete
- Publish the artifact

The pipeline is automatically run when any change is made to either the develop or master branches

## Release pipeline
My release pipeline consists of a single stage:

**Deploy Azure App Service:**

In this stage the artifact from the build is deployed to the app service.

The release pipeline is run whenever a build is successfully created from the master branch. 
