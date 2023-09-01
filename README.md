# :rocket: Quick and Easy Guide to Install Axis Connector in GNS3 :rocket:

This guide provides a quick and straightforward method for installing the Axis Connector in GNS3. Before proceeding, make sure to download the Connector OVA file from the management portal of your Axis workspace/tenant.

## :bookmark_tabs: Table of Contents

1. [Uploading the Axis OVF and Converting to qcow2](#uploading-the-axis-ovf-and-converting-to-qcow2)
2. [Creating GNS3 Template for Axis Connector](#creating-gns3-template-for-axis-connector)
3. [Console Access to Appliance](#console-access-to-appliance)

---

## :arrow_forward: Uploading the Axis OVF and Converting to qcow2

### Step 1: SSH to GNS3 VM and Access the CLI
SSH into your GNS3 VM using the default credentials (`gns3/gns3`) and open the CLI.
```bash
ssh gns3@gns3vm_ip_address
