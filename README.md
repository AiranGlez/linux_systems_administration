![](https://img.shields.io/badge/Microverse-blueviolet)

# LINUX SYSTEMS ADMINISTRATION

> Learning about Linux systems administration.

![screenshot](./app_screenshot.png)

Additional description about the project and its features.

## Built With

- Ubuntu 20.04.2.0 LTS

## Getting Started

### Prerequisites

### Setup

### Install

### Usage

### Run tests

### Deployment

### Virtualization

* How to KVM backup and restore virtual machines

    - List all virtual machines: `virsh list -all`
    - Shutdown the virtual machine to backup: `virsh shutdown VMNAME`
    - Backup VM definition (XML): `virsh dumpxml VMNAME > /mybackup/VMNAME.xml`
    - Find where VM disk is located: `virsh domblklist VMNAME`
    - Backup VM disk (qcow2): `cp /var/lib/libvirt/images/VMNAME.qcow2 /mybackup/VMNAME.qcow2`
    
    NOTE: You can do the backup process without turning off the machines, but it may be healthy to turn it off and on despite errors or data loss. Of course, if the machine should not be interrupted service, as I said VM opened backup can take.

    - To restore VM disk, copy the backup image to its location: `cp /MyBackup/VMNAME.qcow2 var/lib/libvirt/images/`
    - To restore VM, define it from backup XML: `virsh define -file /mybackup/VMNAME.xml`
    - Start VM: `virsh start VMNAME`

## Authors

👤 **Author1**

- GitHub: [@githubhandle](https://github.com/githubhandle)
- Twitter: [@twitterhandle](https://twitter.com/twitterhandle)
- LinkedIn: [LinkedIn](https://linkedin.com/linkedinhandle)

👤 **Author2**

- GitHub: [@githubhandle](https://github.com/githubhandle)
- Twitter: [@twitterhandle](https://twitter.com/twitterhandle)
- LinkedIn: [LinkedIn](https://linkedin.com/linkedinhandle)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](issues/).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Hat tip to anyone whose code was used
- Inspiration
- etc

## 📝 License

This project is [MIT](lic.url) licensed.
