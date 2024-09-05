---
title: Installing OmniOS
weight: 4
---

# Installation

The OmniOS installer is not an application that can be run from within another operating system. Instead, download the OmniOS installation file, burn it to the media associated with its file type and size (CD, DVD, or USB), and boot the system to install from the inserted media.

The Installer can also be booted over the network.

> OmniOS supports AMD64, with work being done to support ARM64.

## Download OmniOS

Installation files are available in several formats, compressed with [xz(1)](https://man.freebsd.org/cgi/man.cgi?query=xz&sektion=1&format=html) or uncompressed. The formats vary depending on media type.

You can start by [downloading OmniOS](https://omnios.org/download.html). The main image types are:

- ISO images (ending with `.iso`) can be used to boot into using CD.
- USB images (ending with `.usb-dd`) can be used to flash a USB drive to boot a bare-metal server.
- Cloud Images (ending with `.cloud.vmdk`) can be used to run an already-installed OmniOS system on the cloud or in a Virtual Machine.
- PXE images (ending with `.zfs.xz`) can be used to boot from the network (more about that later).

## Hardware Requirements

OmniOS is designed to be run on server class systems rather than laptops or generic workstations. You may have luck with this hardware, but there is a good chance you will find your hardware unsupported.

A list of supported hardware is on the [illumos Hardware Compatibility List](http://illumos.org/hcl).

The following configuration is recommended minimum hardware requirements.

|              |      |
| :----------: | :--: |
| Architecture | 64-bit (x86-64) |
| Memory Size  | 1GiB (minimum)  |
| Hard Disk    | 8GiB (minimum)  |


## Pre-Installation Tasks

> 💡 TIP
>
> Consider using virtualization if you want to use OmniOS on a system that already has another operating system installed.

Before moving on to the installation, check that the system is ready by verifying the items in this checklist:

1. **Back Up Important Data**: Before installing any operating system, **always** backup all important data first. Do not store the backup on the system being installed. Instead, save the data to a removable disk such as a USB drive, another system on the network, or an online backup service. Test the backup before starting the installation to make sure it contains all of the needed files. Once the installer formats the system’s disk, all data stored on that disk will be lost.
2. **Decide Where to Install OmniOS**: Make sure you know the answers to the following questions:
3. **Collect Network Information**: Your network probably uses DHCP, but if it does not, make sure you obtain the following information:
   1. IP address
   2. Subnet mask
   3. IP address of default gateway
   4. Domain name of the network, if any
   5. IP addresses of the network’s DNS servers

### Prepare the Installation Media

#### Verify Checksum on macOS

1. Open Terminal and navigate to the ISO's directory.
2. View the checksum file:
   `cat omnios-r151050.iso.sha256`
3. Generate the SHA-256 checksum:
   `shasum -a 256 omnios-r151050.iso`
4. Compare the two checksums.

#### Verify Checksum on \*BSD and Linux

1. Open a terminal and navigate to the ISO's directory.
2. View the checksum file:
   `cat omnios-r151050.iso.sha256`
3. Generate the checksum:
   `sha256sum omnios-r151050.iso`
4. Compare the checksums.

#### Verify Checksum on Windows

1. Open PowerShell and run:
   `Get-FileHash omnios-r151050.iso -Algorithm SHA256`
2. Compare the output with the checksum file.

### Writing the Image File to USB

**Prerequisites**

- USB flash drive - (1GB or larger).
- Download the OmniOS USB installer image.

> 🚨 Before proceeding, back up any important data on the USB stick. This procedure will erase the existing data on the stick.

Before writing the OmniOS USB installer image, you need to identify the USB drive path.

| Operating System | Command              | Device               |
| ---------------- | -------------------- | -------------------- |
| FreeBSD          | `camcontrol devlist` | `/dev/da*`           |
| Linux            | `lsblk` or `blkid`   | `/dev/sd*`           |
| macOS            | `diskutil list`      | `/dev/disk*`         |
| illumos          | `rmformat -l`        | `/dev/rdsk/c*t*d*p0` |



## Starting The Installation



## Troubleshooting



