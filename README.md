# packer-alpine
Packer template for alpine linux

Build a virtual machine image for [Alpine linux](http://www.alpinelinux.org) using [Packer](https://www.packer.io).

    packer build alpine.json

This Packer template will build a [VirtualBox](https://www.virtualbox.org) VM (OVA) from an Alpine ISO image. Networking is configured for DHCP and an SSH user is created (default `vagrant` password `letmein!1234`) with sudo privileges.

You can customize this login

    packer build -var=ssh_username=youruser -var=ssh_password=yourpassword

Further customization is possible by overriding other variables, or editing `alpine.json` or `http/answers`.
