# CrashCart

CrashCart is a portable Raspberry Pi Zero-based homelab recovery and infrastructure toolkit inspired by retro game cartridges and classic service tools.

## Philosophy

CrashCart is intentionally distinct from:

- Gridrunner → mobile sensing and cyberdeck platform
- ControlPlane → orchestration and management platform

CrashCart focuses on:

- infrastructure recovery
- serial console access
- USB gadget tooling
- portable diagnostics
- emergency administration
- deployment assistance
- offline recovery utilities

## Core Hardware Target

- Raspberry Pi Zero v1.3
- USB OTG gadget mode
- UART/serial adapters
- Optional OLED display
- Portable USB-stick style enclosure

## Planned Features

### USB Gadget Modes
- USB Ethernet gadget
- Serial gadget
- Composite gadget support
- Storage emulation
- HID automation for authorized administrative workflows

### Recovery Tooling
- Serial console toolkit
- Proxmox recovery helpers
- UniFi/UDM recovery scripts
- Disk diagnostics
- Backup utilities
- Networking diagnostics

### Cartridge System
CrashCart uses “cartridge profiles” to enable modular operating modes:

- Recovery Cart
- Console Cart
- NetRunner Cart
- BootPak
- Diagnostics Cart

## Project Structure

```text
crashcart/
├── ansible/
├── cartridge-profiles/
├── docs/
├── hardware/
├── scripts/
├── webui/
└── recovery-tools/
```

## License

TBD
