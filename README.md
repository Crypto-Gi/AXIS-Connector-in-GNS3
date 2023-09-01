# 🚀 Axis Connector for GNS3

> A streamlined guide to integrating Axis Connector within your GNS3 environment.

![Axis Connector for GNS3 Logo](your-logo-or-image-link-here)

---

## 📋 Table of Contents

1. [📦 Uploading and Conversion](#uploading-and-conversion)
2. [🛠 GNS3 Template](#gns3-template)
3. [🖥 Console Access](#console-access)

---

## 📦 Uploading and Conversion

### 🛠 SSH to GNS3 VM

```bash
ssh gns3@your-gns3-vm-ip
```
## 📂 Navigate to QEMU Directory
```bash
cd /opt/gns3/images/QEMU
```

## 📤 Upload OVA File

Use `SCP` or similar tools to upload the `axis-connector-centos-nci.ovf` to `/opt/gns3/images/QEMU`.

---

## 🗃 Extract VMDK

Run the following bash commands to extract the VMDK:

```bash
tar xvf axis-connector-centos-nci.ovf
```

Verify the files: ls | grep axis

## 🔄 Rename & Remove Files
```bash
mv axis-connector-centos-nci-docker-v3.28.1-disk1.vmdk axis.vmdk
rm -rf axis-connector-centos-nci*
```

## 🚀 Convert to qcow2
```bash
qemu-img convert -f vmdk -O qcow2 axis.vmdk axis.qcow2
rm -f axis.vmdk
```

## 🛠 GNS3 Template

### 📝 Create QEMU VM

Name: Axis-Connector

QEMU Binary: 

/bin/qemu-system-x86_64(v4.2.1)

RAM: 2048 MB or 4096 MB

Console Type : VNC

Disk Image:
axis.qcow2



