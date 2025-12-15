# Ansible-Notes
What it says on the tin!

## Key Components

- Control Node - Where you install and run Ansible
- Managed Node(s) - These are the machines you want to configure or Automate

### Control Node

- Contains the Anisble Engine
- Stores the Inventory, Playbooks, Roles and Modules
- Executes tasks on remote systems using:
  - SSH (Linux/macOS)
  - WinRM (Windows)
- Recommended to Install on Linux Distributions, but also on
  - macOS via Homebrew
  - Containers (suitable for CI/CD, isolated testing)
  - Cloud-Based Environments with OS which supports Ansible

### Managed Nodes

- Don't need Ansible installed (no agent)
  - Only need to be accessible via SSH or WinRM
- Locations/Names are defined in an inventory file on the control node
- Ansible might need to conduct admin tasks such when it connects (Installing software, creating users, etc..)
  - Sudo privileges for Linux and MacOS
  - Admin Account on Windows (via WinRM)