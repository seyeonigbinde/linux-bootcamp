# Lab 1: Install a LAMP stack on an Azure Linux VM

1. Create a resource group
   {
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack",
   "location": "eastus",
   "managedBy": null,
   "name": "LAMP-Stack",
   "properties": {
   "provisioningState": "Succeeded"
   },
   "tags": null,
   "type": "Microsoft.Resources/resourceGroups"
   }
2. Create a virtual machine
   {
   "fqdns": "",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Compute/virtualMachines/seyeVM",
   "location": "eastus",
   "macAddress": "00-0D-3A-8A-5F-F6",
   "powerState": "VM running",
   "privateIpAddress": "10.0.0.4",
   "publicIpAddress": "20.120.13.205",
   "resourceGroup": "LAMP-Stack",
   "zones": ""
   }
3. Open port 80 for web traffic
   {
   "defaultSecurityRules": [
   {
   "access": "Allow",
   "description": "Allow inbound traffic from all VMs in VNET",
   "destinationAddressPrefix": "VirtualNetwork",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "_",
   "destinationPortRanges": [],
   "direction": "Inbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowVnetInBound",
   "name": "AllowVnetInBound",
   "priority": 65000,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "VirtualNetwork",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   },
   {
   "access": "Allow",
   "description": "Allow inbound traffic from azure load balancer",
   "destinationAddressPrefix": "_",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "_",
   "destinationPortRanges": [],
   "direction": "Inbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowAzureLoadBalancerInBound",
   "name": "AllowAzureLoadBalancerInBound",
   "priority": 65001,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "AzureLoadBalancer",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   },
   {
   "access": "Deny",
   "description": "Deny all inbound traffic",
   "destinationAddressPrefix": "_",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "_",
   "destinationPortRanges": [],
   "direction": "Inbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/DenyAllInBound",
   "name": "DenyAllInBound",
   "priority": 65500,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "_",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   },
   {
   "access": "Allow",
   "description": "Allow outbound traffic from all VMs to all VMs in VNET",
   "destinationAddressPrefix": "VirtualNetwork",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "_",
   "destinationPortRanges": [],
   "direction": "Outbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowVnetOutBound",
   "name": "AllowVnetOutBound",
   "priority": 65000,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "VirtualNetwork",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   },
   {
   "access": "Allow",
   "description": "Allow outbound traffic from all VMs to Internet",
   "destinationAddressPrefix": "Internet",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "_",
   "destinationPortRanges": [],
   "direction": "Outbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowInternetOutBound",
   "name": "AllowInternetOutBound",
   "priority": 65001,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "_",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   },
   {
   "access": "Deny",
   "description": "Deny all outbound traffic",
   "destinationAddressPrefix": "_",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "_",
   "destinationPortRanges": [],
   "direction": "Outbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/DenyAllOutBound",
   "name": "DenyAllOutBound",
   "priority": 65500,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "_",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   }
   ],
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "flowLogs": null,
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG",
   "location": "eastus",
   "name": "seyeVMNSG",
   "networkInterfaces": [
   {
   "dnsSettings": null,
   "dscpConfiguration": null,
   "enableAcceleratedNetworking": null,
   "enableIpForwarding": null,
   "etag": null,
   "extendedLocation": null,
   "hostedWorkloads": null,
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkInterfaces/seyeVMVMNic",
   "ipConfigurations": null,
   "location": null,
   "macAddress": null,
   "migrationPhase": null,
   "name": null,
   "networkSecurityGroup": null,
   "nicType": null,
   "primary": null,
   "privateEndpoint": null,
   "privateLinkService": null,
   "provisioningState": null,
   "resourceGroup": "LAMP-Stack",
   "resourceGuid": null,
   "tags": null,
   "tapConfigurations": null,
   "type": null,
   "virtualMachine": null,
   "workloadType": null
   }
   ],
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "resourceGuid": "eb46b361-a5f4-482d-9215-e9a00ced7bce",
   "securityRules": [
   {
   "access": "Allow",
   "description": null,
   "destinationAddressPrefix": "_",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "22",
   "destinationPortRanges": [],
   "direction": "Inbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/securityRules/default-allow-ssh",
   "name": "default-allow-ssh",
   "priority": 1000,
   "protocol": "Tcp",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "_",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/securityRules"
   },
   {
   "access": "Allow",
   "description": null,
   "destinationAddressPrefix": "_",
   "destinationAddressPrefixes": [],
   "destinationApplicationSecurityGroups": null,
   "destinationPortRange": "80",
   "destinationPortRanges": [],
   "direction": "Inbound",
   "etag": "W/\"402b7dbb-6418-41b4-b911-8b67df0169f6\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/LAMP-Stack/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/securityRules/open-port-80",
   "name": "open-port-80",
   "priority": 900,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "LAMP-Stack",
   "sourceAddressPrefix": "_",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "\*",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/securityRules"
   }
   ],
   "subnets": null,
   "tags": {},
   "type": "Microsoft.Network/networkSecurityGroups"
   }
4. SSH into your VM
5. Install Apache, MySQL, and PHP
   Welcome to the MySQL monitor. Commands end with ; or \g.
   Your MySQL connection id is 4
   Server version: 5.7.36-0ubuntu0.18.04.1 (Ubuntu)

Copyright (c) 2000, 2021, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>

6. Install WordPress

CREATE DATABASE wordpress;
GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,ALTER
ON wordpress.\*
TO wordpress@localhost
IDENTIFIED BY 'Richard03$$';

### Notes:

Tutorial: Install a LAMP stack on an Azure Linux VM

- https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-lamp-stack

Sample Gist

- https://gist.github.com/mikepfeiffer/96d659042f0575a617648a33c92b8f4a

Build and run a web application with the MEAN stack on an Azure Linux virtual machine

- https://docs.microsoft.com/en-us/learn/modules/build-a-web-app-with-mean-on-a-linux-vm/

MEAN Stack App

- https://github.com/MicrosoftDocs/mslearn-build-a-web-app-with-mean-on-a-linux-vm

# MEAN Stack using Sandbox

{
"fqdns": "",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Compute/virtualMachines/MeanStack",
"location": "westus",
"macAddress": "00-0D-3A-3B-21-86",
"powerState": "VM running",
"privateIpAddress": "10.0.0.4",
"publicIpAddress": "104.42.45.62",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"zones": ""
}

{
"defaultSecurityRules": [
{
"access": "Allow",
"description": "Allow inbound traffic from all VMs in VNET",
"destinationAddressPrefix": "VirtualNetwork",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "_",
"destinationPortRanges": [],
"direction": "Inbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/defaultSecurityRules/AllowVnetInBound",
"name": "AllowVnetInBound",
"priority": 65000,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "VirtualNetwork",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
},
{
"access": "Allow",
"description": "Allow inbound traffic from azure load balancer",
"destinationAddressPrefix": "_",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "_",
"destinationPortRanges": [],
"direction": "Inbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/defaultSecurityRules/AllowAzureLoadBalancerInBound",
"name": "AllowAzureLoadBalancerInBound",
"priority": 65001,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "AzureLoadBalancer",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
},
{
"access": "Deny",
"description": "Deny all inbound traffic",
"destinationAddressPrefix": "_",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "_",
"destinationPortRanges": [],
"direction": "Inbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/defaultSecurityRules/DenyAllInBound",
"name": "DenyAllInBound",
"priority": 65500,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "_",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
},
{
"access": "Allow",
"description": "Allow outbound traffic from all VMs to all VMs in VNET",
"destinationAddressPrefix": "VirtualNetwork",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "_",
"destinationPortRanges": [],
"direction": "Outbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/defaultSecurityRules/AllowVnetOutBound",
"name": "AllowVnetOutBound",
"priority": 65000,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "VirtualNetwork",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
},
{
"access": "Allow",
"description": "Allow outbound traffic from all VMs to Internet",
"destinationAddressPrefix": "Internet",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "_",
"destinationPortRanges": [],
"direction": "Outbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/defaultSecurityRules/AllowInternetOutBound",
"name": "AllowInternetOutBound",
"priority": 65001,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "_",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
},
{
"access": "Deny",
"description": "Deny all outbound traffic",
"destinationAddressPrefix": "_",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "_",
"destinationPortRanges": [],
"direction": "Outbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/defaultSecurityRules/DenyAllOutBound",
"name": "DenyAllOutBound",
"priority": 65500,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "_",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
}
],
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"flowLogs": null,
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG",
"location": "westus",
"name": "MeanStackNSG",
"networkInterfaces": [
{
"dnsSettings": null,
"dscpConfiguration": null,
"enableAcceleratedNetworking": null,
"enableIpForwarding": null,
"etag": null,
"extendedLocation": null,
"hostedWorkloads": null,
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkInterfaces/MeanStackVMNic",
"ipConfigurations": null,
"location": null,
"macAddress": null,
"migrationPhase": null,
"name": null,
"networkSecurityGroup": null,
"nicType": null,
"primary": null,
"privateEndpoint": null,
"privateLinkService": null,
"provisioningState": null,
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"resourceGuid": null,
"tags": null,
"tapConfigurations": null,
"type": null,
"virtualMachine": null,
"vnetEncryptionSupported": null,
"workloadType": null
}
],
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"resourceGuid": "b490cef3-0521-4523-b6ac-03d3c74d1ae4",
"securityRules": [
{
"access": "Allow",
"description": null,
"destinationAddressPrefix": "_",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "22",
"destinationPortRanges": [],
"direction": "Inbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/securityRules/default-allow-ssh",
"name": "default-allow-ssh",
"priority": 1000,
"protocol": "Tcp",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "_",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "_",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/securityRules"
},
{
"access": "Allow",
"description": null,
"destinationAddressPrefix": "_",
"destinationAddressPrefixes": [],
"destinationApplicationSecurityGroups": null,
"destinationPortRange": "80",
"destinationPortRanges": [],
"direction": "Inbound",
"etag": "W/\"068a2144-f4a8-4a28-b49a-4eba0b32b6a0\"",
"id": "/subscriptions/81dd920a-15a9-47b2-a1f5-7779019bc7f4/resourceGroups/learn-af999c31-420b-492c-b802-69c3410acc89/providers/Microsoft.Network/networkSecurityGroups/MeanStackNSG/securityRules/open-port-80",
"name": "open-port-80",
"priority": 900,
"protocol": "_",
"provisioningState": "Succeeded",
"resourceGroup": "learn-af999c31-420b-492c-b802-69c3410acc89",
"sourceAddressPrefix": "_",
"sourceAddressPrefixes": [],
"sourceApplicationSecurityGroups": null,
"sourcePortRange": "\*",
"sourcePortRanges": [],
"type": "Microsoft.Network/networkSecurityGroups/securityRules"
}
],
"subnets": null,
"tags": {},
"type": "Microsoft.Network/networkSecurityGroups"
}

# Create an SSH connection to your VM.

The authenticity of host '104.42.45.62 (104.42.45.62)' can't be established.
ECDSA key fingerprint is SHA256:LkfwGDXQqzYhEqCqSfG0KIZhbfqD1IdJclq5cixpgO4.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '104.42.45.62' (ECDSA) to the list of known hosts.
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.11.0-1022-azure x86_64)

- Documentation: https://help.ubuntu.com
- Management: https://landscape.canonical.com
- Support: https://ubuntu.com/advantage

System information as of Tue Dec 14 08:36:20 UTC 2021

System load: 0.0 Processes: 112
Usage of /: 4.7% of 28.90GB Users logged in: 0
Memory usage: 7% IPv4 address for eth0: 10.0.0.4
Swap usage: 0%

1 update can be applied immediately.
To see these additional updates run: apt list --upgradable

The list of available updates is more than a week old.
To check for new updates run: sudo apt update

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/\*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

# Install the MongoDB package.

mongodb.service - An object/document-oriented database
Loaded: loaded (/lib/systemd/system/mongodb.service; enabled; vendo>
Active: active (running) since Tue 2021-12-14 08:41:34 UTC; 26s ago
Docs: man:mongod(1)
Main PID: 19170 (mongod)
Tasks: 23 (limit: 4107)
Memory: 43.3M
CGroup: /system.slice/mongodb.service
└─19170 /usr/bin/mongod --unixSocketPrefix=/run/mongodb --c>

Dec 14 08:41:34 MeanStack systemd[1]: Started An object/document-oriente>
