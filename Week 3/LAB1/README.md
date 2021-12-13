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
