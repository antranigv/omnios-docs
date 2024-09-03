---
title: Introduction
weight: 3
---

# Introduction

Thank you for choosing OmniOS! In this chapter will cover the following

- The goals of the OmniOS Project.
- What OmniOS can do.
- How OmniOS is developed

## Project Goals

As mentioned in the _OmniOS: Motivation and Design_ presentation, the goals of the project are the following

- Just Enough Operating System: OmniOS has the tooling required to build itself
- ABI Stability: old software runs on new installations
- ZFS: OmniOS can run root-on-ZFS, supports ZFS Boot Environments, fault management, administrative delegation and more
- Zones: completely isolated virtual servers within a single operating system instance
- DTrace: comprehensive dynamic [tracing](https://en.wikipedia.org/wiki/Tracing_(software)) framework for debugging production systems

## OmniOS Usage

OmniOS has a large collection of software and subsystems, which allows it to be used as:

- Web server
- File server
- Email server
- Storage server
- Virtualization server
- And more...

## OmniOS Development

The development of OmniOS happens on [GitHub](https://github.com/omniosorg), here are a list of some important repositories:

- [omni](https://github.com/omniosorg/omni): Tools to automate the setup and maintenance of an OmniOS build server or zone.
- [omnios-build](https://github.com/omniosorg/omnios-build): Build system for OmniOS
- [omnios-extra](https://github.com/omniosorg/omnios-extra): Extra packages for OmniOS
- [kayak](https://github.com/omniosorg/kayak): PXE-enabled network imaging of OmniOS

Anyone is welcome to fork, modify and send PRs to the OmniOS project!