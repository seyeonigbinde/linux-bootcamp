# Lab 1: Create a Linux virtual machine with the Azure CLI

1. Launch Azure Cloud Shell
   [
   {
   "cloudName": "AzureCloud",
   "homeTenantId": "1b35b349-42bc-42f4-9f79-714bab535268",
   "id": "d2653dbd-1995-4aba-8a53-fd1fd943c124",
   "isDefault": true,
   "managedByTenants": [],
   "name": "Azure subscription 1",
   "state": "Enabled",
   "tenantId": "1b35b349-42bc-42f4-9f79-714bab535268",
   "user": {
   "name": "seyeonigbinde@gmail.com",
   "type": "user"
   }
   }
   ]
2. Create a resource group
   {
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup",
   "location": "eastus",
   "managedBy": null,
   "name": "seyeResourceGroup",
   "properties": {
   "provisioningState": "Succeeded"
   },
   "tags": null,
   "type": "Microsoft.Resources/resourceGroups"
   }
3. Create virtual machine
   {
   "fqdns": "",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Compute/virtualMachines/seyeVM",
   "location": "eastus",
   "macAddress": "00-22-48-2C-D2-45",
   "powerState": "VM running",
   "privateIpAddress": "10.0.0.4",
   "publicIpAddress": "20.124.248.163",
   "resourceGroup": "seyeResourceGroup",
   "zones": ""
   }
4. Open port 80 for web traffic
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowVnetInBound",
   "name": "AllowVnetInBound",
   "priority": 65000,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowAzureLoadBalancerInBound",
   "name": "AllowAzureLoadBalancerInBound",
   "priority": 65001,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/DenyAllInBound",
   "name": "DenyAllInBound",
   "priority": 65500,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowVnetOutBound",
   "name": "AllowVnetOutBound",
   "priority": 65000,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/AllowInternetOutBound",
   "name": "AllowInternetOutBound",
   "priority": 65001,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/defaultSecurityRules/DenyAllOutBound",
   "name": "DenyAllOutBound",
   "priority": 65500,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
   "sourceAddressPrefix": "_",
   "sourceAddressPrefixes": [],
   "sourceApplicationSecurityGroups": null,
   "sourcePortRange": "_",
   "sourcePortRanges": [],
   "type": "Microsoft.Network/networkSecurityGroups/defaultSecurityRules"
   }
   ],
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "flowLogs": null,
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG",
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
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkInterfaces/seyeVMVMNic",
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
   "resourceGroup": "seyeResourceGroup",
   "resourceGuid": null,
   "tags": null,
   "tapConfigurations": null,
   "type": null,
   "virtualMachine": null,
   "workloadType": null
   }
   ],
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
   "resourceGuid": "a09007ab-0ff6-43d1-994b-438f781864b3",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/securityRules/default-allow-ssh",
   "name": "default-allow-ssh",
   "priority": 1000,
   "protocol": "Tcp",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
   "etag": "W/\"9645ec79-0f08-44dd-9d9c-7310cea985b2\"",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroup/providers/Microsoft.Network/networkSecurityGroups/seyeVMNSG/securityRules/open-port-80",
   "name": "open-port-80",
   "priority": 900,
   "protocol": "_",
   "provisioningState": "Succeeded",
   "resourceGroup": "seyeResourceGroup",
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
5. Connect to virtual machine
   Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 5.4.0-1063-azure x86_64)

- Documentation: https://help.ubuntu.com
- Management: https://landscape.canonical.com
- Support: https://ubuntu.com/advantage

System information as of Thu Nov 18 21:52:19 UTC 2021

System load: 0.01 Processes: 112
Usage of /: 4.7% of 28.90GB Users logged in: 0
Memory usage: 5% IP address for eth0: 10.0.0.4
Swap usage: 0%

0 updates can be applied immediately.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/\*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details. 6. Install web server
azureuser@seyeVM:~$ sudo apt-get -y update
Hit:1 http://azure.archive.ubuntu.com/ubuntu bionic InRelease
Get:2 http://azure.archive.ubuntu.com/ubuntu bionic-updates InRelease [88.7 kB]
Get:3 http://azure.archive.ubuntu.com/ubuntu bionic-backports InRelease [74.6 kB]
Get:4 http://security.ubuntu.com/ubuntu bionic-security InRelease [88.7 kB]
Get:5 http://azure.archive.ubuntu.com/ubuntu bionic/universe amd64 Packages [8570 kB]
Get:6 http://azure.archive.ubuntu.com/ubuntu bionic/universe Translation-en [4941 kB]
Get:7 http://azure.archive.ubuntu.com/ubuntu bionic/multiverse amd64 Packages [151 kB]  
Get:8 http://azure.archive.ubuntu.com/ubuntu bionic/multiverse Translation-en [108 kB]
Get:9 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 Packages [2303 kB]
Get:10 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main Translation-en [445 kB]
Get:11 http://azure.archive.ubuntu.com/ubuntu bionic-updates/restricted amd64 Packages [540 kB]
Get:12 http://azure.archive.ubuntu.com/ubuntu bionic-updates/restricted Translation-en [73.6 kB]
Get:13 http://azure.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 Packages [1766 kB]
Get:14 http://azure.archive.ubuntu.com/ubuntu bionic-updates/universe Translation-en [381 kB]
Get:15 http://azure.archive.ubuntu.com/ubuntu bionic-updates/multiverse amd64 Packages [27.3 kB]
Get:16 http://azure.archive.ubuntu.com/ubuntu bionic-updates/multiverse Translation-en [6808 B]
Get:17 http://azure.archive.ubuntu.com/ubuntu bionic-backports/main amd64 Packages [10.0 kB]
Get:18 http://azure.archive.ubuntu.com/ubuntu bionic-backports/main Translation-en [4764 B]
Get:19 http://azure.archive.ubuntu.com/ubuntu bionic-backports/universe amd64 Packages [10.3 kB]
Get:20 http://azure.archive.ubuntu.com/ubuntu bionic-backports/universe Translation-en [4588 B]
Get:21 http://security.ubuntu.com/ubuntu bionic-security/main amd64 Packages [1958 kB]
Get:22 http://security.ubuntu.com/ubuntu bionic-security/main Translation-en [352 kB]
Get:23 http://security.ubuntu.com/ubuntu bionic-security/restricted amd64 Packages [516 kB]
Get:24 http://security.ubuntu.com/ubuntu bionic-security/restricted Translation-en [69.9 kB]
Get:25 http://security.ubuntu.com/ubuntu bionic-security/universe amd64 Packages [1150 kB]
Get:26 http://security.ubuntu.com/ubuntu bionic-security/universe Translation-en [264 kB]
Get:27 http://security.ubuntu.com/ubuntu bionic-security/multiverse amd64 Packages [20.9 kB]
Get:28 http://security.ubuntu.com/ubuntu bionic-security/multiverse Translation-en [4732 B]
Fetched 23.9 MB in 5s (5287 kB/s)  
Reading package lists... Done
azureuser@seyeVM:~$ sudo apt-get -y install nginx
Reading package lists... Done
Building dependency tree  
Reading state information... Done
The following package was automatically installed and is no longer required:
linux-headers-4.15.0-162
Use 'sudo apt autoremove' to remove it.
The following additional packages will be installed:
fontconfig-config fonts-dejavu-core libfontconfig1 libgd3 libjbig0 libjpeg-turbo8 libjpeg8 libnginx-mod-http-geoip libnginx-mod-http-image-filter
libnginx-mod-http-xslt-filter libnginx-mod-mail libnginx-mod-stream libtiff5 libwebp6 libxpm4 nginx-common nginx-core
Suggested packages:
libgd-tools fcgiwrap nginx-doc ssl-cert
The following NEW packages will be installed:
fontconfig-config fonts-dejavu-core libfontconfig1 libgd3 libjbig0 libjpeg-turbo8 libjpeg8 libnginx-mod-http-geoip libnginx-mod-http-image-filter
libnginx-mod-http-xslt-filter libnginx-mod-mail libnginx-mod-stream libtiff5 libwebp6 libxpm4 nginx nginx-common nginx-core
0 upgraded, 18 newly installed, 0 to remove and 9 not upgraded.
Need to get 2461 kB of archives.
After this operation, 8210 kB of additional disk space will be used.
Get:1 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libjpeg-turbo8 amd64 1.5.2-0ubuntu5.18.04.4 [110 kB]
Get:2 http://azure.archive.ubuntu.com/ubuntu bionic/main amd64 fonts-dejavu-core all 2.37-1 [1041 kB]
Get:3 http://azure.archive.ubuntu.com/ubuntu bionic/main amd64 fontconfig-config all 2.12.6-0ubuntu2 [55.8 kB]
Get:4 http://azure.archive.ubuntu.com/ubuntu bionic/main amd64 libfontconfig1 amd64 2.12.6-0ubuntu2 [137 kB]
Get:5 http://azure.archive.ubuntu.com/ubuntu bionic/main amd64 libjpeg8 amd64 8c-2ubuntu8 [2194 B]
Get:6 http://azure.archive.ubuntu.com/ubuntu bionic/main amd64 libjbig0 amd64 2.1-3.1build1 [26.7 kB]
Get:7 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libtiff5 amd64 4.0.9-5ubuntu0.4 [153 kB]
Get:8 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libwebp6 amd64 0.6.1-2ubuntu0.18.04.1 [186 kB]
Get:9 http://azure.archive.ubuntu.com/ubuntu bionic/main amd64 libxpm4 amd64 1:3.5.12-1 [34.0 kB]
Get:10 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libgd3 amd64 2.2.5-4ubuntu0.5 [119 kB]
Get:11 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 nginx-common all 1.14.0-0ubuntu1.9 [37.2 kB]
Get:12 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libnginx-mod-http-geoip amd64 1.14.0-0ubuntu1.9 [11.0 kB]
Get:13 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libnginx-mod-http-image-filter amd64 1.14.0-0ubuntu1.9 [14.3 kB]
Get:14 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libnginx-mod-http-xslt-filter amd64 1.14.0-0ubuntu1.9 [12.7 kB]
Get:15 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libnginx-mod-mail amd64 1.14.0-0ubuntu1.9 [41.6 kB]
Get:16 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libnginx-mod-stream amd64 1.14.0-0ubuntu1.9 [63.5 kB]
Get:17 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 nginx-core amd64 1.14.0-0ubuntu1.9 [413 kB]
Get:18 http://azure.archive.ubuntu.com/ubuntu bionic-updates/main amd64 nginx all 1.14.0-0ubuntu1.9 [3596 B]
Fetched 2461 kB in 0s (48.3 MB/s)
Preconfiguring packages ...
Selecting previously unselected package libjpeg-turbo8:amd64.
(Reading database ... 76986 files and directories currently installed.)
Preparing to unpack .../00-libjpeg-turbo8_1.5.2-0ubuntu5.18.04.4_amd64.deb ...
Unpacking libjpeg-turbo8:amd64 (1.5.2-0ubuntu5.18.04.4) ...
Selecting previously unselected package fonts-dejavu-core.
Preparing to unpack .../01-fonts-dejavu-core_2.37-1_all.deb ...
Unpacking fonts-dejavu-core (2.37-1) ...
Selecting previously unselected package fontconfig-config.
Preparing to unpack .../02-fontconfig-config_2.12.6-0ubuntu2_all.deb ...
Unpacking fontconfig-config (2.12.6-0ubuntu2) ...
Selecting previously unselected package libfontconfig1:amd64.
Preparing to unpack .../03-libfontconfig1_2.12.6-0ubuntu2_amd64.deb ...
Unpacking libfontconfig1:amd64 (2.12.6-0ubuntu2) ...
Selecting previously unselected package libjpeg8:amd64.
Preparing to unpack .../04-libjpeg8_8c-2ubuntu8_amd64.deb ...
Unpacking libjpeg8:amd64 (8c-2ubuntu8) ...
Selecting previously unselected package libjbig0:amd64.
Preparing to unpack .../05-libjbig0_2.1-3.1build1_amd64.deb ...
Unpacking libjbig0:amd64 (2.1-3.1build1) ...
Selecting previously unselected package libtiff5:amd64.
Preparing to unpack .../06-libtiff5_4.0.9-5ubuntu0.4_amd64.deb ...
Unpacking libtiff5:amd64 (4.0.9-5ubuntu0.4) ...
Selecting previously unselected package libwebp6:amd64.
Preparing to unpack .../07-libwebp6_0.6.1-2ubuntu0.18.04.1_amd64.deb ...
Unpacking libwebp6:amd64 (0.6.1-2ubuntu0.18.04.1) ...
Selecting previously unselected package libxpm4:amd64.
Preparing to unpack .../08-libxpm4_1%3a3.5.12-1_amd64.deb ...
Unpacking libxpm4:amd64 (1:3.5.12-1) ...
Selecting previously unselected package libgd3:amd64.
Preparing to unpack .../09-libgd3_2.2.5-4ubuntu0.5_amd64.deb ...
Unpacking libgd3:amd64 (2.2.5-4ubuntu0.5) ...
Selecting previously unselected package nginx-common.
Preparing to unpack .../10-nginx-common_1.14.0-0ubuntu1.9_all.deb ...
Unpacking nginx-common (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package libnginx-mod-http-geoip.
Preparing to unpack .../11-libnginx-mod-http-geoip_1.14.0-0ubuntu1.9_amd64.deb ...
Unpacking libnginx-mod-http-geoip (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package libnginx-mod-http-image-filter.
Preparing to unpack .../12-libnginx-mod-http-image-filter_1.14.0-0ubuntu1.9_amd64.deb ...
Unpacking libnginx-mod-http-image-filter (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package libnginx-mod-http-xslt-filter.
Preparing to unpack .../13-libnginx-mod-http-xslt-filter_1.14.0-0ubuntu1.9_amd64.deb ...
Unpacking libnginx-mod-http-xslt-filter (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package libnginx-mod-mail.
Preparing to unpack .../14-libnginx-mod-mail_1.14.0-0ubuntu1.9_amd64.deb ...
Unpacking libnginx-mod-mail (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package libnginx-mod-stream.
Preparing to unpack .../15-libnginx-mod-stream_1.14.0-0ubuntu1.9_amd64.deb ...
Unpacking libnginx-mod-stream (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package nginx-core.
Preparing to unpack .../16-nginx-core_1.14.0-0ubuntu1.9_amd64.deb ...
Unpacking nginx-core (1.14.0-0ubuntu1.9) ...
Selecting previously unselected package nginx.
Preparing to unpack .../17-nginx_1.14.0-0ubuntu1.9_all.deb ...
Unpacking nginx (1.14.0-0ubuntu1.9) ...
Setting up libjbig0:amd64 (2.1-3.1build1) ...
Setting up fonts-dejavu-core (2.37-1) ...
Setting up nginx-common (1.14.0-0ubuntu1.9) ...
Created symlink /etc/systemd/system/multi-user.target.wants/nginx.service → /lib/systemd/system/nginx.service.
Setting up libjpeg-turbo8:amd64 (1.5.2-0ubuntu5.18.04.4) ...
Setting up libnginx-mod-mail (1.14.0-0ubuntu1.9) ...
Setting up libxpm4:amd64 (1:3.5.12-1) ...
Setting up libnginx-mod-http-xslt-filter (1.14.0-0ubuntu1.9) ...
Setting up libnginx-mod-http-geoip (1.14.0-0ubuntu1.9) ...
Setting up libwebp6:amd64 (0.6.1-2ubuntu0.18.04.1) ...
Setting up libjpeg8:amd64 (8c-2ubuntu8) ...
Setting up fontconfig-config (2.12.6-0ubuntu2) ...
Setting up libnginx-mod-stream (1.14.0-0ubuntu1.9) ...
Setting up libtiff5:amd64 (4.0.9-5ubuntu0.4) ...
Setting up libfontconfig1:amd64 (2.12.6-0ubuntu2) ...
Setting up libgd3:amd64 (2.2.5-4ubuntu0.5) ...
Setting up libnginx-mod-http-image-filter (1.14.0-0ubuntu1.9) ...
Setting up nginx-core (1.14.0-0ubuntu1.9) ...
Setting up nginx (1.14.0-0ubuntu1.9) ...
Processing triggers for systemd (237-3ubuntu10.52) ...
Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
Processing triggers for ufw (0.36-0ubuntu0.18.04.1) ...
Processing triggers for ureadahead (0.100.0-21) ...
Processing triggers for libc-bin (2.27-3ubuntu1.4) ... 7. View the web server in action

### Notes:

Quickstart: Create a Linux VM

- https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli

Quickstart for Bash in Azure Cloud Shell

- https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart
