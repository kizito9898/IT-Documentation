# macOS Documentation

## What is macOS?

macOS is the proprietary Unix-based operating system developed by Apple Inc. It is designed to run on Macintosh (Mac) computers.

Unlike Microsoft Windows, macOS combines an intuitive graphical user interface (GUI) with powerful command-line capabilities, making it suitable for both everyday users and IT professionals.

---

# Project Objective

The goal of this project is to configure and document a fully functional virtualized macOS environment (macOS 15 Sequoia) using a VMware hypervisor on standard Windows hardware.

This project also serves as a learning platform to:

- Master macOS installation and configuration
- Understand system administration workflows
- Develop technical support skills for macOS environments

---

# Why Learn macOS for IT Support?

To provide private and enterprise-level technical support, technicians must possess a strong understanding of multiple operating systems rather than relying on a single platform.

Understanding macOS enables technicians to:

- Confidently troubleshoot end-user issues
- Support mixed operating system environments
- Expand their technical skill set
- Increase employability in modern IT environments

---
# Benefits of Learning macOS

Learning macOS provides access to enterprise environments where multiple operating systems coexist.

Advantages include:

- Supporting Apple devices alongside Windows and Linux systems
- Gaining experience with enterprise IT administration
- Understanding the Apple ecosystem
- Working with macOS-specific management tools
- Building knowledge of Apple's security architecture

This knowledge helps technicians transition smoothly into modern IT support roles and Managed Service Provider (MSP) environments.

# Getting Started with macOS Installation

## Overview

Before installing macOS Sequoia in a virtual environment, several prerequisite tools and packages must be downloaded and installed. These tools are required to prepare the virtualization environment and support the macOS installation process.

---

# Prerequisites

The following software must be installed before proceeding:

- Python 3
- QEMU
- VMware Workstation Pro
- OCVM (OpenCore VMware Package)
- OpenCorePkg

---

# Installing Python 3

Python is required by several scripts used during the macOS installation process.

## Steps

1. Visit the official Python website:
   - https://www.python.org
2. Download the latest stable release of **Python 3**.
3. Run the installer.
4. Complete the installation wizard.

---

# Installing QEMU

QEMU provides virtualization components required during the macOS setup.

## Steps

1. Visit the official download page:
   - https://qemu.weilnetz.de/w64/
2. Download the latest stable Windows release.
3. Launch the installer.
4. Complete the QEMU installation wizard.
5. Verify that QEMU has been installed successfully.

---

# Installing VMware Workstation Pro

VMware Workstation Pro is used as the virtualization platform for running macOS.

## Steps

1. Visit the official VMware website.
2. Download the latest version of **VMware Workstation Pro**.
3. Complete any required registration.
4. Download and install the software.

> For this lab environment, VMware Workstation Pro was already installed from previous virtualization projects.

---

# Downloading OCVM

The next package required is **OCVM (OpenCore VMware Package)**.

GitHub Repository:

- https://github.com/DrDonk/OCVM/releases

## Steps

1. Open the GitHub releases page.
2. Download the latest stable release.
3. For this project, Version **3.0** was selected.
4. Extract the downloaded package.

---

# Understanding OpenCore

OpenCore is a sophisticated bootloader that injects and patches configuration data in memory rather than modifying files directly on disk.

Using OpenCore makes it possible to achieve a near-native macOS experience on unsupported hardware and virtual machines.

## Benefits

- Near-native macOS performance
- Improved compatibility
- Flexible boot configuration
- Better support for newer macOS releases

For the best compatibility, always download the latest stable release unless your lab specifically requires an older version.

---

# Downloading OpenCorePkg

OpenCorePkg contains the OpenCore bootloader and supporting files required during the installation process.

GitHub Repository:

- https://github.com/acidanthera/OpenCorePkg

## Steps

1. Navigate to the GitHub repository.
2. Download the latest release.
3. Extract the package.
4. Prepare the files for the macOS installation process.