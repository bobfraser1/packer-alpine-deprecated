# packer-alpine

## DEPRECATED

This repo has been deprecated and renamed. The new packer-alpine will use an Apache 2.0 license. This repo is for anyone to use the existing code to date under the MIT license.

Packer template for alpine linux

Build a virtual machine image for [Alpine linux](https://www.alpinelinux.org) using [Packer](https://www.packer.io).

    packer build alpine.json

This Packer template will build a [VirtualBox](https://www.virtualbox.org) VM (OVA) from an Alpine ISO image. Networking is configured for DHCP and an SSH user is created (default `vagrant` password `vagrant`) with sudo privileges.

**Security Note:** The Vagrant [insecure public key](https://github.com/hashicorp/vagrant/tree/master/keys) has been added. You can override `ssh_key` to provide your own secure ssh key.

You can customize this login

    packer build -var=ssh_username=youruser -var=ssh_password=yourpassword

Further customization is possible by overriding other variables, or editing `alpine.json` or `http/answers`.

## Vagrant Ready

[Vagrant](https://vagrantup.com) is not required to build the image. However, the image can easily be turned into a [Vagrant Base Box](https://www.vagrantup.com/docs/boxes/base).
