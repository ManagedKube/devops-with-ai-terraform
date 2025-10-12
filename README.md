# devops-with-ai-terraform
How to run a production cloud system with AI

## The idea behind this
Github and the community has been building and using AI for a little while.  With DevOps and building infrastructure
with IaC, we have found that just chatting with an AI bot, it lacks context even if you give it the file you are
currently working on.  It doesnt know the wider context of your DevOps repo and how it is setup and used.  Luckily,
Github and the community has created an ecosystem to help with this context problem.  However, it is still very much
in it's early stages and how things works is a moving target.  This repository will showcase what we have been doing
and how we have been doing it.  From our experience with real world production system and using AI to build it, we
are rolling our learnings back into this repo.  We have found that with the right pieces in place and the right
content, AI can dramatically reduce our work and help us to build our cloud infrastructure.

## What Works Well with AI Agents

- Creating a new Terraform module
- Updating a Terraform modules with additional feature(s)
- Churning out the Terraform instantiation of the Terraform modules instances (staging, prod, etc)
- You will most likely test in staging and then once that has been figured out (hopefully with your AI assistant)
  you can open an issue for the AI to update prod with the same changes to the same versions, etc

## Demo

### Updating production with the same release version as staging
???

### Updating a Terraform module with ??something??
??? Create a github issue to update a terraform module with something (make it interesting and kinda complex).  Then
assign it to copilot.  Make sure the PR is good, if not, iterate on it.  Then post the issue and PR here.

## How to make Github Copilot better
- https://github.blog/ai-and-ml/github-copilot/5-tips-for-writing-better-custom-instructions-for-copilot/
- https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-repository-instructions
