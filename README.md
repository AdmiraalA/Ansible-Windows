# Windows VM Cloning and Configuration with Ansible

This project automates the process of cloning a Windows VM, configuring it with required settings, and activating its license using Ansible. It supports:

- Injecting `unattend.xml` for first-boot configuration.
- Installing and enabling OpenSSH or WinRM for remote management.
- Activating Windows via KMS or a product key.
- Configuring Active Directory Domain Services.

## Structure

### Playbooks
- **clone-and-configure.yml**: Orchestrates cloning and configuration tasks.

### Roles
1. **clone_vm**: Clones the VM and injects the unattend file.
2. **activate_windows**: Activates Windows with a product key or KMS.
3. **directory_services**: Installs and configures Active Directory.

### Templates
- **unattend.j2**: Template for generating `unattend.xml`.
