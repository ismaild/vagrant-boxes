# Cent-OS Vagrant Base Boxes

## Downloads

## How these boxes were built

These boxes were automatically built using [veewee](https://github.com/jedi4ever/veewee) (0.4.5.1) and the definitions in this repo. 

The definitions are stock veewee definitions for a minimal CentOS installation, with the following changes:
* modified so the disk can grow to 200GB and provide 2.5GB of swap.
* Removed chef & puppet

```sh
$ veewee vbox define CentOS-6.4-x86_64 CentOS-6.4-x86_64-minimal
$ veewee vbox build CentOS-6.4-x86_64
# Eject the disks from the running VM and shutdown.
$ vagrant package --base CentOS-6.4-x86_64 --output CentOS-6.4-x86_64-v20131103.box
```
