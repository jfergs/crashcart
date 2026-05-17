# CrashCart Backlog

Project-local backlog for CrashCart. Keep implementation details here and roll
up only cross-project dependencies to `workspace-tracker`.

## Current State

- Repository has the project identity and initial feature outline.
- Target hardware is Raspberry Pi Zero v1.3 with USB OTG gadget support.
- Planned domains are USB gadget modes, serial console access, diagnostics,
  recovery tooling, and modular cartridge profiles.

## High Priority

- Define the first recovery cartridge MVP.
  - Select one target workflow, such as serial console recovery or USB Ethernet
    diagnostics.
  - Document required hardware, cables, and host operating systems.
  - Create a minimal command checklist that works without network access.

- Scaffold the repo layout.
  - Add directories for `scripts/`, `docs/`, `hardware/`,
    `cartridge-profiles/`, and `recovery-tools/`.
  - Add a simple script entry point for local diagnostics.
  - Add a smoke-test path that can run on macOS without Pi hardware.

- Design USB gadget configuration.
  - Document Ethernet, serial, storage, and composite gadget modes.
  - Decide whether modes are selected by config file, cartridge profile, or CLI.
  - Capture safe rollback steps so the Pi remains reachable after changes.

- Establish Raspberry Pi image setup.
  - Pick base OS image and minimum package set.
  - Define first-boot configuration for hostname, SSH, USB OTG, and local user.
  - Add setup notes for read-only or resilient storage if needed.

## Medium Priority

- Add recovery scripts.
  - Network diagnostics.
  - Serial console helpers.
  - Proxmox/UniFi recovery notes.
  - Disk and filesystem inspection helpers.

- Add cartridge profile format.
  - Define metadata fields, enabled services, scripts, and operator notes.
  - Add example profiles: Recovery Cart, Console Cart, NetRunner Cart.

- Add optional OLED/status display plan.
  - Define the minimum status fields worth showing.
  - Keep display support optional until core recovery workflows are stable.

## Validation

- Boot a Pi Zero with the setup steps.
- Confirm USB Ethernet gadget appears on macOS and Linux hosts.
- Confirm serial console access works with a known target.
- Confirm every recovery script fails safely when required hardware is missing.
