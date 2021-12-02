# Fedora Tools for Packer

## List Packages

1. RPM Development Tools
2. fedora-packager

## Official Documentation

1. [RPM Packaging](https://developer.fedoraproject.org/deployment/rpm/about.html)
2. [Creating RPM packages](https://docs.fedoraproject.org/en-US/quick-docs/creating-rpm-packages/)
3. [Fcch Custom Packages](https://blog.fcch.xyz) - In progress
    
## Run Command

```bash
## Create a container
$ docker run --name demo -h demo -it fcch/fedora-packer-rpm:35
## Create a container after exit destroy
$ docker run --rm -it fcch/fedora-packer-rpm:35
## Create a container after exit destroy with hostname
$ docker run --rm -h demo -it fcch/fedora-packer-rpm:35
```