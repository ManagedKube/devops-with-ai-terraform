# devops-with-ai-terraform
This repository is here to show how to run your devops practice with ai and more specifically, this repository is focused on building 
your infrastructure with terraform in a cloud (aws, gcp, azure, etc).  The way that this repository does things are not always the easiest
methods but it uses methods and processes that has been battled tested in many production environments over 10+ years.  This is not just
a demo repository.  It is a repository where someone can take this and run a real large scale production cloud environment with.  We
previously had https://github.com/ManagedKube/kubernetes-ops which is what this repository is but without the AI part.  AI has come a long
way and we now recommend using AI to help you to run your infrastructure.  

## Tech stack in use
The IaC (infrastructure as code) being used here is Terraform.

### Terraform modules
Most of the logic used are encapsulated in Terraform Modules.  By putting all of the logic into terraform modules, it makes it more tidy,
easier to test, and use.  A terraform module should have a specific purpose.  For example, it can create a VPC with everything it usually
needs like public subnets, private subnets, nat, default security groups, routes, etc.  The modules should be flexible enough for a bunch
of use cases but we tend to not make it so flexible that it solves all use cases because that would make the module very complex.  A right
balance of flexibility and a few path makes this manageable. We tend to only make modules that we cannot find a well known public module
for.  No need to reinvent the wheel here if there is already something out there that is widely used.

### Terraform environments
There can be one or more terraform environments and they use the terraform modules to instantiate each component with.  It can use one or
more of the terraform modules here in this repository or public ones.

### Deployment CI/CD
Uses Github Actions for CI/CD

### Testing
Uses Github Actions for testing

## Project and code guidelines


## Project structure

## Resources

