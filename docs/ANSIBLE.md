# CrashCart Ansible Management

CrashCart uses Ansible for provisioning and cartridge deployment.

## Goals

- Idempotent configuration
- Offline deployment support
- Cartridge profile switching
- Repeatable recovery images

## Planned Structure

```text
ansible/
├── inventory/
├── playbooks/
├── roles/
└── group_vars/
```

## Planned Playbooks

### base.yml
Base system provisioning.

### usb-gadget.yml
USB gadget mode configuration.

### serial-cart.yml
Serial recovery toolkit.

### network-cart.yml
Networking diagnostics tools.

### lockdown.yml
Security and hardening configuration.
