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

## Project and Code Guidelines

### Code Quality
- **Type Hints**: Always use type hints in languages that support them (especially Python)
- **File Paths**: When suggesting code changes, always include the file path
- **Testing**: Write tests for new components and validate changes before committing

### Security Best Practices
- **Encryption**: Use encryption by default when possible
- **Key Management**: Provide options for users to pass in encryption keys (KMS, certificates, etc.) OR create them automatically
- **Network Security**: Give options for public or private IP addresses where applicable
- **Secrets**: Never commit secrets; use GitHub Actions secrets and variables

### Resource Tagging
- Add tags to all AWS resources indicating:
  - What created the resource (e.g., `created_by: terraform`)
  - The environment (e.g., `environment: staging`)

## Configuration Management

### Using GitHub Actions for Configuration
All production configuration is managed through GitHub Actions to avoid local setup requirements.


### Standard Deployment Process
1. **Preview**: Review changes using `terraform plan` (automatic on PRs)
2. **Apply**: Deploy changes with `terraform apply` (automatic on merge to main)
3. **Monitor**: logs

### GitHub Actions Automation
- **Pull Requests**: Automatically runs `terraform plan` and posts results as PR comment
- **Merge to Main**: Automatically runs `terraform apply` to apply infrastructure changes

## Testing and Validation

### Before Making Changes
1. Understand the existing component structure
2. Review related components and their dependencies
3. Check for existing tests or validation patterns

### After Making Changes
1. **Lint**: Run linters if available for the changed files
2. **Validate**: Use `terraform plan` to see planned changes
3. **Test**: Verify in staging environment before production
4. **Document**: Update README or component documentation if needed

### Component Testing
- Test components in staging environment first
- Use pre-releases for testing new component versions
- Validate that existing stacks are not inadvertently affected

## Project structure




## Resources

