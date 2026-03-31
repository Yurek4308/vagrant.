# Vagrant Practical Task

## 📌 Description

This repository contains a Vagrant configuration file used to create and manage a virtual machine environment.

## ⚙️ Vagrantfile Explanation

### config.vm.box

Specifies the base image (box) used for the virtual machine.
In this project, **ubuntu/jammy64** is used.

### config.vm.network

Configures networking for the virtual machine.
A private network with a static IP address is assigned.

### config.vm.provision

Defines provisioning steps.
A shell script is used to:

* update package lists
* install nginx web server

### $install_deps

This variable contains the shell script executed during provisioning.

## 🚀 How to Run

```bash
vagrant up
```

## 🔐 Access VM

```bash
vagrant ssh
```

## 🛑 Stop VM

```bash
vagrant halt
```

## ❌ Destroy VM

```bash
vagrant destroy -f
```

## 📷 Proof of Work

Screenshots or video demonstration are provided via Google Drive link.
