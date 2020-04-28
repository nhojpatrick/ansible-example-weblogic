# Ansible Example of WebLogic

## Requirements

  * Vagrant v2.2.7 (may work with any v2.x)
  * VirtualBox v6.1.6 (may work with any v6.x)

### Java 8 update 192

1. Visit: https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html
1. Download: jdk-8u192-linux-x64.rpm
1. Copy/Move to: `provisioning/files`

### WebLogic 12.1.3.0.0

1. Visit: https://www.oracle.com/middleware/technologies/weblogic-server-downloads.html
1. Download: fmw_12.1.3.0.0_wls.jar i.e. 12.1.3 Generic (881 MB) Download
1. Copy/Move to: `provisioning/files`

## Tested Combinations

The following have been tested, other combinations might work;

- Vagrant v2.2.7 + VirtualBox v6.1.6 + CentOS 7 + Java 8u192 + WebLogic 12.1.3.0.0

## Quick Start

Simple as, ` vagrant up`, and a new vm will be created, with Java 8 and WebLogic 12.1.3 installed.

## Notes

The files `setup_*.yaml` are used as a work around to install the latest version of ansible, including git so that ansible galaxy can install from github.

This setup uses a patch version of the ansible galaxy role 'lean_delivery.weblogic'. The patch allows for a software only installation.

  - Patched Version https://github.com/nhojpatrick/lean-delivery_ansible-role-weblogic/tree/software-install-only
  - Origional Version https://github.com/lean-delivery/ansible-role-weblogic
