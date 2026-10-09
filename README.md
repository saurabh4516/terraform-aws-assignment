# Terraform AWS Assignment

**Name:** Saurabh Pawar
**Course:** DevOps Institute Mumbai (in association with IIT Patna), Assignment 5, Week 9-10
**Cloud / Region:** AWS, us-west-2 (Oregon)
**Instance type:** t3.micro (free tier eligible)

## Completed tutorials

| # | Tutorial | Folder | Key learning |
|---|----------|--------|--------------|
| 3 | Build Infrastructure | `03-build` | The `provider` block tells Terraform which cloud to talk to, and the `resource` block describes what to create. The `init`, `plan`, `apply` cycle downloads the provider, previews the changes, and then creates the EC2 instance. Terraform records what it created in the state file. I used a `data "aws_ami"` block to look up the latest Ubuntu AMI instead of hardcoding an AMI ID, so it works in any region. |
| 4 | Change Infrastructure | `04-change` | Terraform compares my configuration with the real infrastructure and shows only the difference. Changing the `Name` tag showed `~ update in-place`, and the instance ID stayed the same, so the server was not recreated. Changes to some arguments, such as the AMI, would show `-/+` and force a destroy and recreate. |
| 5 | Destroy Infrastructure | `05-destroy` | `terraform destroy` removes every resource tracked in the state file, after showing a plan and asking for `yes`. I ran it after each tutorial so that the EC2 instance stops and does not cost money. |

## Repository structure
