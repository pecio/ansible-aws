# Experiment with Ansible and AWS

## Contents

### Playbooks

- `playbook.yml`: Creates an AlmaLinux OS 10 instance for each entry in `inventory`, installs Nginx and sets up a sample page.
- `windows.yml`: Creates a Windows Server 2025 Core Edition instance for each entry in `inventory`, installs Nginx and sets up a sample page.
- `terminate.yml`: Terminates each instance whose name is in `inventory`.

### Additional files

- `ansible.cfg`: Configures Ansible to use `inventory` as inventory source and silences Python detection warning.
- `index.hmtl.j2`: Jinja2 template for the sample page.
- `inventory`: The list of instance names to create and configure.
- `LICENSE`: MIT License
- `mise.toml`: [Mise-en-place](https://mise.en.dev) configuration for installing Ansible Core
- `README.md`: This file

## Requirements

- Pip package `boto3`.
- AWS CLI installed and configured
- AWS Session Manager Plugin
- A supported Ansible Core version (currently 2.19, 2.20, 2.21)
- `SSM_BUCKET` environment variable with the name of an S3 Bucket we have access to (versioning disabled recommended)
