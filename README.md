# learn-terraform-azure
# Terraform best practices
1. Manipulate State only through TF commands
2. Always set up a shared remote storage for the state file (It can be stored in azure storage accounts, terraform cloud, google cloud, amazon S3 bucket etc)
3. Use State locking. Lock state file until writing of state file is completed.
4. Back up your state files (by enabling versioning for it)
5. Use 1 state per Environment (Dev, QA and Prod)
6. Host Terraform Code in its own Git repository.
7. CI of terraform code. Treat Terraform Code like your application code. (Review and Test code ) 
8. Apply Infrastructure Changes only through CD pipeline.
9. Use Terraform modules to reuse code, specially when creating multiple resources or working with multiple environments.
10. Use loops like count and for_each to optimize repetitive resource creation inside your modules, like creating multiple subnets with just one block of resource code.
11. Try not to hardcode values inside your resources blocks. Use variables instead and centralize the values with terraform.tfvars file.
12
