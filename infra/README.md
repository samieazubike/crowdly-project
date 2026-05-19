# infra/

Purpose: Infrastructure-as-code for deployments, CI, and environment configuration.

What to add here:

- Terraform / Pulumi / CloudFormation templates for cloud resources.
- CI/CD manifests (GitHub Actions workflows or other CI) to build contracts, run tests, and deploy frontend/backends.
- Notes for secret provisioning and remote state management.

Important:

- Do not commit provider credentials or cloud secrets. Use remote state encryption and access control.
