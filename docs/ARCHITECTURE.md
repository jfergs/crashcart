# CrashCart Architecture

## Overview

CrashCart is a lightweight field recovery appliance built around Raspberry Pi Zero hardware and USB gadget mode.

The system is designed as:

- a portable crash cart
- a serial recovery appliance
- a USB gadget utility system
- a modular recovery toolkit

## Design Goals

- Fast boot
- Low power
- Portable
- Minimal dependencies
- Reliable offline operation
- Immutable/recoverable system state

## System Components

### Base OS
- Raspberry Pi OS Lite
- Read-only filesystem support
- OverlayFS experimentation
- Watchdog auto-recovery

### USB Gadget Layer
Provides:
- Ethernet gadget
- Serial gadget
- Composite modes
- Storage emulation

### Cartridge Profiles
Profiles configure:
- enabled services
- installed packages
- USB modes
- recovery tools
- UI modules

### Recovery Toolkit
Includes:
- tmux
- SSH
- networking tools
- serial console tools
- disk diagnostics
- backup scripts

## Distinction From Other Projects

### Gridrunner
Gridrunner is focused on:
- mobile sensing
- distributed telemetry
- RF experimentation
- cyberdeck workflows

CrashCart is focused on:
- infrastructure recovery
- administration
- diagnostics
- serial access

### ControlPlane
ControlPlane is focused on:
- orchestration
- dashboards
- APIs
- management

CrashCart is focused on:
- field recovery
- offline tooling
- portable infrastructure access
