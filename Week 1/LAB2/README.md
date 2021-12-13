# Lab 2: Manage Linux VMs with the Azure CLI

1. Create resource group
   {
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroupVM",
   "location": "eastus",
   "managedBy": null,
   "name": "seyeResourceGroupVM",
   "properties": {
   "provisioningState": "Succeeded"
   },
   "tags": null,
   "type": "Microsoft.Resources/resourceGroups"
   }
2. Create virtual machine
   {
   "fqdns": "",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroupVM/providers/Microsoft.Compute/virtualMachines/seyeVM",
   "location": "eastus",
   "macAddress": "00-0D-3A-19-C3-C9",
   "powerState": "VM running",
   "privateIpAddress": "10.0.0.4",
   "publicIpAddress": "20.124.14.247",
   "resourceGroup": "seyeResourceGroupVM",
   "zones": ""
   }
3. Connect to VM
   Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 5.4.0-1063-azure x86_64)

- Documentation: https://help.ubuntu.com
- Management: https://landscape.canonical.com
- Support: https://ubuntu.com/advantage

System information as of Thu Nov 18 22:20:29 UTC 2021

System load: 0.0 Processes: 107
Usage of /: 4.6% of 28.90GB Users logged in: 0
Memory usage: 5% IP address for eth0: 10.0.0.4
Swap usage: 0%

0 updates can be applied immediately.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/\*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

4. Understand VM images
   {
   "offer": "secured-lamp-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lamp-on-centos",
   "urn": "cognosys:secured-lamp-on-centos:secured-lamp-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-lamp-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lamp-on-centos",
   "urn": "cognosys:secured-lamp-on-centos:secured-lamp-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-lamp-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lamp-on-centos",
   "urn": "cognosys:secured-lamp-on-centos:secured-lamp-on-centos:1.2.1",
   "version": "1.2.1"
   },
   {
   "offer": "secured-lamp-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lamp-on-centos",
   "urn": "cognosys:secured-lamp-on-centos:secured-lamp-on-centos:1.2.2",
   "version": "1.2.2"
   },
   {
   "offer": "centos8",
   "publisher": "tunnelbiz",
   "sku": "centos8minimal",
   "urn": "tunnelbiz:centos8:centos8minimal:1.9.10",
   "version": "1.9.10"
   },
   {
   "offer": "centos8",
   "publisher": "tunnelbiz",
   "sku": "centos8minimal",
   "urn": "tunnelbiz:centos8:centos8minimal:1.9.11",
   "version": "1.9.11"
   },
   {
   "offer": "centos8",
   "publisher": "tunnelbiz",
   "sku": "centos8minimal",
   "urn": "tunnelbiz:centos8:centos8minimal:8.4.0",
   "version": "8.4.0"
   },
   {
   "offer": "dns-server-linux-centos-7-8",
   "publisher": "tidalmediainc",
   "sku": "dns-server-centos-7",
   "urn": "tidalmediainc:dns-server-linux-centos-7-8:dns-server-centos-7:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "centos8",
   "publisher": "tunnelbiz",
   "sku": "centos8streamminimal",
   "urn": "tunnelbiz:centos8:centos8streamminimal:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "secured-lamp-on-centos-m10",
   "publisher": "cognosys",
   "sku": "secured-lamp-on-centos-mariadb10",
   "urn": "cognosys:secured-lamp-on-centos-m10:secured-lamp-on-centos-mariadb10:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "docker-community-edition-centos",
   "publisher": "tidalmediainc",
   "sku": "docker-community-edition-centos-8",
   "urn": "tidalmediainc:docker-community-edition-centos:docker-community-edition-centos-8:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "centos8lamp",
   "publisher": "tunnelbiz",
   "sku": "centos8lamp",
   "urn": "tunnelbiz:centos8lamp:centos8lamp:0.0.2",
   "version": "0.0.2"
   },
   {
   "offer": "secured-lapp-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lapp-on-centos",
   "urn": "cognosys:secured-lapp-on-centos:secured-lapp-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-lapp-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lapp-on-centos",
   "urn": "cognosys:secured-lapp-on-centos:secured-lapp-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "docker-community-edition-centos7",
   "publisher": "tidalmediainc",
   "sku": "docker-community-edition-7",
   "urn": "tidalmediainc:docker-community-edition-centos7:docker-community-edition-7:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "centos8optimize",
   "publisher": "tunnelbiz",
   "sku": "centos8optimize",
   "urn": "tunnelbiz:centos8optimize:centos8optimize:2020.08.05",
   "version": "2020.08.05"
   },
   {
   "offer": "secured-lime-survey-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lime-survey-on-centos",
   "urn": "cognosys:secured-lime-survey-on-centos:secured-lime-survey-on-centos:1.1.0",
   "version": "1.1.0"
   },
   {
   "offer": "secured-lime-survey-on-centos",
   "publisher": "cognosys",
   "sku": "secured-lime-survey-on-centos",
   "urn": "cognosys:secured-lime-survey-on-centos:secured-lime-survey-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "centos8optimize",
   "publisher": "tunnelbiz",
   "sku": "centos8optimizedev",
   "urn": "tunnelbiz:centos8optimize:centos8optimizedev:2020.08.05",
   "version": "2020.08.05"
   },
   {
   "offer": "minecraft-bedrock-centos-8",
   "publisher": "tidalmediainc",
   "sku": "minecraft-bedrock-centos-8",
   "urn": "tidalmediainc:minecraft-bedrock-centos-8:minecraft-bedrock-centos-8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-live-helper-chat-on-centos",
   "publisher": "cognosys",
   "sku": "secured-live-helper-chat-on-centos",
   "urn": "cognosys:secured-live-helper-chat-on-centos:secured-live-helper-chat-on-centos:1.1.0",
   "version": "1.1.0"
   },
   {
   "offer": "secured-live-helper-chat-on-centos",
   "publisher": "cognosys",
   "sku": "secured-live-helper-chat-on-centos",
   "urn": "cognosys:secured-live-helper-chat-on-centos:secured-live-helper-chat-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "centos8withdotnet",
   "publisher": "tunnelbiz",
   "sku": "aspnetcoreruntime",
   "urn": "tunnelbiz:centos8withdotnet:aspnetcoreruntime:0.1.2",
   "version": "0.1.2"
   },
   {
   "offer": "centos8withdotnet",
   "publisher": "tunnelbiz",
   "sku": "aspnetcoreruntime",
   "urn": "tunnelbiz:centos8withdotnet:aspnetcoreruntime:0.1.3",
   "version": "0.1.3"
   },
   {
   "offer": "minecraft-bedrock-centos-8-minimal",
   "publisher": "tidalmediainc",
   "sku": "minecraft-bedrock-centos-8-minimal",
   "urn": "tidalmediainc:minecraft-bedrock-centos-8-minimal:minecraft-bedrock-centos-8-minimal:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-magento-on-centos",
   "publisher": "cognosys",
   "sku": "secured-magento-on-centos",
   "urn": "cognosys:secured-magento-on-centos:secured-magento-on-centos:1.1.0",
   "version": "1.1.0"
   },
   {
   "offer": "secured-magento-on-centos",
   "publisher": "cognosys",
   "sku": "secured-magento-on-centos",
   "urn": "cognosys:secured-magento-on-centos:secured-magento-on-centos:1.2.1",
   "version": "1.2.1"
   },
   {
   "offer": "secured-magento-on-centos",
   "publisher": "cognosys",
   "sku": "secured-magento-on-centos",
   "urn": "cognosys:secured-magento-on-centos:secured-magento-on-centos:1.2.2",
   "version": "1.2.2"
   },
   {
   "offer": "secured-magento-on-centos",
   "publisher": "cognosys",
   "sku": "secured-magento-on-centos",
   "urn": "cognosys:secured-magento-on-centos:secured-magento-on-centos:1.2.3",
   "version": "1.2.3"
   },
   {
   "offer": "minecraft-java-centos-7",
   "publisher": "tidalmediainc",
   "sku": "minecraft-java-server-centos-7",
   "urn": "tidalmediainc:minecraft-java-centos-7:minecraft-java-server-centos-7:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "secured-mahara-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-mahara-on-centos-7-3",
   "urn": "cognosys:secured-mahara-on-centos:new-secured-mahara-on-centos-7-3:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "minecraft-java-centos-7-minimal",
   "publisher": "tidalmediainc",
   "sku": "minecraft-java-centos-7-minimal",
   "urn": "tidalmediainc:minecraft-java-centos-7-minimal:minecraft-java-centos-7-minimal:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-mantis-on-centos",
   "publisher": "cognosys",
   "sku": "secured-mantis-on-centos",
   "urn": "cognosys:secured-mantis-on-centos:secured-mantis-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-mantis-on-centos",
   "publisher": "cognosys",
   "sku": "secured-mantis-on-centos",
   "urn": "cognosys:secured-mantis-on-centos:secured-mantis-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "centos-8-minimal-edition",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "centos-8-minimal-edition",
   "urn": "virtualpulsesro1607008728942:centos-8-minimal-edition:centos-8-minimal-edition:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "minecraft-java-centos-8-minimal",
   "publisher": "tidalmediainc",
   "sku": "minecraft-java-centos-8-minimal",
   "urn": "tidalmediainc:minecraft-java-centos-8-minimal:minecraft-java-centos-8-minimal:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "centos_7_docker_c_e",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "centos_7_docker_c_e",
   "urn": "virtualpulsesro1607008728942:centos_7_docker_c_e:centos_7_docker_c_e:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-mautic-on-centos",
   "publisher": "cognosys",
   "sku": "secured-mautic-on-centos",
   "urn": "cognosys:secured-mautic-on-centos:secured-mautic-on-centos:1.0.3",
   "version": "1.0.3"
   },
   {
   "offer": "secured-mautic-on-centos",
   "publisher": "cognosys",
   "sku": "secured-mautic-on-centos",
   "urn": "cognosys:secured-mautic-on-centos:secured-mautic-on-centos:1.1.0",
   "version": "1.1.0"
   },
   {
   "offer": "minecraft-java-linux-centos-8",
   "publisher": "tidalmediainc",
   "sku": "minecraft-java-centos-8",
   "urn": "tidalmediainc:minecraft-java-linux-centos-8:minecraft-java-centos-8:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "centos_7_minimal_edition",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "centos_7_minimal_edition",
   "urn": "virtualpulsesro1607008728942:centos_7_minimal_edition:centos_7_minimal_edition:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "secured-media-wiki-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-media-wiki-on-centos-7-3-basic-lic",
   "urn": "cognosys:secured-media-wiki-on-centos:new-secured-media-wiki-on-centos-7-3-basic-lic:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "mongo-db-linux-centos-8",
   "publisher": "tidalmediainc",
   "sku": "mongo-db-linux-centos-8",
   "urn": "tidalmediainc:mongo-db-linux-centos-8:mongo-db-linux-centos-8:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "secured-modx-on-centos",
   "publisher": "cognosys",
   "sku": "secured-modx-on-centos",
   "urn": "cognosys:secured-modx-on-centos:secured-modx-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-modx-on-centos",
   "publisher": "cognosys",
   "sku": "secured-modx-on-centos",
   "urn": "cognosys:secured-modx-on-centos:secured-modx-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-modx-on-centos",
   "publisher": "cognosys",
   "sku": "secured-modx-on-centos",
   "urn": "cognosys:secured-modx-on-centos:secured-modx-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "centos_7_pure_ftpd_server",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "centos_7_pure_ftpd_server",
   "urn": "virtualpulsesro1607008728942:centos_7_pure_ftpd_server:centos_7_pure_ftpd_server:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "mongodb_centos",
   "publisher": "tidalmediainc",
   "sku": "mongo-db-centos-7",
   "urn": "tidalmediainc:mongodb_centos:mongo-db-centos-7:1.0.5",
   "version": "1.0.5"
   },
   {
   "offer": "secured-ngnix-on-centos-7-3",
   "publisher": "cognosys",
   "sku": "secured-ngnix-on-centos-7-3",
   "urn": "cognosys:secured-ngnix-on-centos-7-3:secured-ngnix-on-centos-7-3:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "moodle-tm-lms-centos-8",
   "publisher": "tidalmediainc",
   "sku": "moodle-system-centos-8",
   "urn": "tidalmediainc:moodle-tm-lms-centos-8:moodle-system-centos-8:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "centos_8_docker_c_e",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "centos_8_docker_c_e",
   "urn": "virtualpulsesro1607008728942:centos_8_docker_c_e:centos_8_docker_c_e:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "secured-noalyss-on-centos",
   "publisher": "cognosys",
   "sku": "secured-noalyss-on-centos",
   "urn": "cognosys:secured-noalyss-on-centos:secured-noalyss-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-noalyss-on-centos",
   "publisher": "cognosys",
   "sku": "secured-noalyss-on-centos",
   "urn": "cognosys:secured-noalyss-on-centos:secured-noalyss-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "centos_8_pure_ftpd_server",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "centos_8_pure_ftpd_server",
   "urn": "virtualpulsesro1607008728942:centos_8_pure_ftpd_server:centos_8_pure_ftpd_server:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "proftp-server-centos",
   "publisher": "tidalmediainc",
   "sku": "proftp-server-centos-7",
   "urn": "tidalmediainc:proftp-server-centos:proftp-server-centos-7:1.0.3",
   "version": "1.0.3"
   },
   {
   "offer": "secured-nodejs-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-node-js-ent-lic",
   "urn": "cognosys:secured-nodejs-on-centos:new-secured-node-js-ent-lic:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-nodejs-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-node-js-ent-lic",
   "urn": "cognosys:secured-nodejs-on-centos:new-secured-node-js-ent-lic:1.2.1",
   "version": "1.2.1"
   },
   {
   "offer": "sftp-open-ssh-centos-7-8",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "sftp-open-ssh-centos-7-8",
   "urn": "virtualpulsesro1607008728942:sftp-open-ssh-centos-7-8:sftp-open-ssh-centos-7-8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "squid-easy-centos-7",
   "publisher": "tidalmediainc",
   "sku": "squid-easy-centos-7",
   "urn": "tidalmediainc:squid-easy-centos-7:squid-easy-centos-7:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-open-cart-on-centos",
   "publisher": "cognosys",
   "sku": "secured-open-cart-on-centos",
   "urn": "cognosys:secured-open-cart-on-centos:secured-open-cart-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-open-cart-on-centos",
   "publisher": "cognosys",
   "sku": "secured-open-cart-on-centos",
   "urn": "cognosys:secured-open-cart-on-centos:secured-open-cart-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "squid-easy-centos-8",
   "publisher": "tidalmediainc",
   "sku": "squid-easy-centos-8",
   "urn": "tidalmediainc:squid-easy-centos-8:squid-easy-centos-8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "sftp_open_ssh_centos_8",
   "publisher": "virtualpulsesro1607008728942",
   "sku": "sftp_open_ssh_centos_8",
   "urn": "virtualpulsesro1607008728942:sftp_open_ssh_centos_8:sftp_open_ssh_centos_8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "squid-easy-server-centos-8-minimal",
   "publisher": "tidalmediainc",
   "sku": "squid-easy-server-centos-8-minimal",
   "urn": "tidalmediainc:squid-easy-server-centos-8-minimal:squid-easy-server-centos-8-minimal:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-orangehrm-on-centos",
   "publisher": "cognosys",
   "sku": "secured-orangehrm-on-centos",
   "urn": "cognosys:secured-orangehrm-on-centos:secured-orangehrm-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-orangehrm-on-centos",
   "publisher": "cognosys",
   "sku": "secured-orangehrm-on-centos",
   "urn": "cognosys:secured-orangehrm-on-centos:secured-orangehrm-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-orangehrm-on-centos",
   "publisher": "cognosys",
   "sku": "secured-orangehrm-on-centos",
   "urn": "cognosys:secured-orangehrm-on-centos:secured-orangehrm-on-centos:1.3.1",
   "version": "1.3.1"
   },
   {
   "offer": "nimble-streamer-centos",
   "publisher": "wmspanel",
   "sku": "nimble-streamer",
   "urn": "wmspanel:nimble-streamer-centos:nimble-streamer:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "nimble-streamer-centos",
   "publisher": "wmspanel",
   "sku": "nimble-streamer",
   "urn": "wmspanel:nimble-streamer-centos:nimble-streamer:1.1.0",
   "version": "1.1.0"
   },
   {
   "offer": "nimble-streamer-centos",
   "publisher": "wmspanel",
   "sku": "nimble-streamer",
   "urn": "wmspanel:nimble-streamer-centos:nimble-streamer:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-osclass-on-centos",
   "publisher": "cognosys",
   "sku": "secured-osclass-on-centos",
   "urn": "cognosys:secured-osclass-on-centos:secured-osclass-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-osclass-on-centos",
   "publisher": "cognosys",
   "sku": "secured-osclass-on-centos",
   "urn": "cognosys:secured-osclass-on-centos:secured-osclass-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "squid-easy-server-webmin-centos-7",
   "publisher": "tidalmediainc",
   "sku": "squid-easy-server-webmin-centos-7",
   "urn": "tidalmediainc:squid-easy-server-webmin-centos-7:squid-easy-server-webmin-centos-7:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-owncloud-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-owncloud-on-centos-basic-lic",
   "urn": "cognosys:secured-owncloud-on-centos:new-secured-owncloud-on-centos-basic-lic:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "squid-easy-server-webmin-centos-8",
   "publisher": "tidalmediainc",
   "sku": "squid-easy-server-webmin-centos-8",
   "urn": "tidalmediainc:squid-easy-server-webmin-centos-8:squid-easy-server-webmin-centos-8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "xilinx_alveo_u250_deployment_vm_centos78_032321",
   "publisher": "xilinx",
   "sku": "xilinx_alveo_u250_deployment_vm_centos78_032321",
   "urn": "xilinx:xilinx_alveo_u250_deployment_vm_centos78_032321:xilinx_alveo_u250_deployment_vm_centos78_032321:4.0.0",
   "version": "4.0.0"
   },
   {
   "offer": "secured-oxid-eshop-on-centos",
   "publisher": "cognosys",
   "sku": "secured-oxid-eshop-on-centos",
   "urn": "cognosys:secured-oxid-eshop-on-centos:secured-oxid-eshop-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-oxid-eshop-on-centos",
   "publisher": "cognosys",
   "sku": "secured-oxid-eshop-on-centos",
   "urn": "cognosys:secured-oxid-eshop-on-centos:secured-oxid-eshop-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "squid-protected-webmin-centos",
   "publisher": "tidalmediainc",
   "sku": "squid-protected-webmin-centos",
   "urn": "tidalmediainc:squid-protected-webmin-centos:squid-protected-webmin-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "xilinx_vitis_2020_2_centos78_development_vm",
   "publisher": "xilinx",
   "sku": "vitis2020_2_1118_1232_centos78",
   "urn": "xilinx:xilinx_vitis_2020_2_centos78_development_vm:vitis2020_2_1118_1232_centos78:2.0.0",
   "version": "2.0.0"
   },
   {
   "offer": "secured-passenger-nginx-on-centos",
   "publisher": "cognosys",
   "sku": "secured-passenger-nginx-on-centos",
   "urn": "cognosys:secured-passenger-nginx-on-centos:secured-passenger-nginx-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-passenger-nginx-on-centos",
   "publisher": "cognosys",
   "sku": "secured-passenger-nginx-on-centos",
   "urn": "cognosys:secured-passenger-nginx-on-centos:secured-passenger-nginx-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "tinyproxy-easy-centos-8",
   "publisher": "tidalmediainc",
   "sku": "tinyproxy-easy-centos-8",
   "urn": "tidalmediainc:tinyproxy-easy-centos-8:tinyproxy-easy-centos-8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-piwigo-gallery-on-centos",
   "publisher": "cognosys",
   "sku": "secured-piwigo-gallery-on-centos",
   "urn": "cognosys:secured-piwigo-gallery-on-centos:secured-piwigo-gallery-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-piwigo-gallery-on-centos",
   "publisher": "cognosys",
   "sku": "secured-piwigo-gallery-on-centos",
   "urn": "cognosys:secured-piwigo-gallery-on-centos:secured-piwigo-gallery-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-piwigo-gallery-on-centos",
   "publisher": "cognosys",
   "sku": "secured-piwigo-gallery-on-centos",
   "urn": "cognosys:secured-piwigo-gallery-on-centos:secured-piwigo-gallery-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "tinyproxy-server-centos-8",
   "publisher": "tidalmediainc",
   "sku": "tinyproxy-server-centos-8",
   "urn": "tidalmediainc:tinyproxy-server-centos-8:tinyproxy-server-centos-8:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-plone-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-plone-on-centos-basic",
   "urn": "cognosys:secured-plone-on-centos:new-secured-plone-on-centos-basic:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-prestashop-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-prestashop-on-centos",
   "urn": "cognosys:secured-prestashop-on-centos:new-secured-prestashop-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-redis-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-redis-on-centos",
   "urn": "cognosys:secured-redis-on-centos:new-secured-redis-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-redmine-on-centos",
   "publisher": "cognosys",
   "sku": "secured-redmine-on-centos",
   "urn": "cognosys:secured-redmine-on-centos:secured-redmine-on-centos:1.1.3",
   "version": "1.1.3"
   },
   {
   "offer": "secured-report-server-on-centos",
   "publisher": "cognosys",
   "sku": "secured-report-server-on-centos",
   "urn": "cognosys:secured-report-server-on-centos:secured-report-server-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-report-server-on-centos",
   "publisher": "cognosys",
   "sku": "secured-report-server-on-centos",
   "urn": "cognosys:secured-report-server-on-centos:secured-report-server-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-resource-space-on-centos",
   "publisher": "cognosys",
   "sku": "secured-resource-space-on-centos",
   "urn": "cognosys:secured-resource-space-on-centos:secured-resource-space-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-resource-space-on-centos",
   "publisher": "cognosys",
   "sku": "secured-resource-space-on-centos",
   "urn": "cognosys:secured-resource-space-on-centos:secured-resource-space-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-round-cube-on-centos",
   "publisher": "cognosys",
   "sku": "secured-round-cube-on-centos",
   "urn": "cognosys:secured-round-cube-on-centos:secured-round-cube-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-ruby-on-centos",
   "publisher": "cognosys",
   "sku": "secured-ruby-on-centos",
   "urn": "cognosys:secured-ruby-on-centos:secured-ruby-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-ruby-on-centos",
   "publisher": "cognosys",
   "sku": "secured-ruby-on-centos",
   "urn": "cognosys:secured-ruby-on-centos:secured-ruby-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-seopanel-on-centos",
   "publisher": "cognosys",
   "sku": "secured-seopanel-on-centos",
   "urn": "cognosys:secured-seopanel-on-centos:secured-seopanel-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-silverstripe-on-centos",
   "publisher": "cognosys",
   "sku": "secured-silverstripe-on-centos",
   "urn": "cognosys:secured-silverstripe-on-centos:secured-silverstripe-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-silverstripe-on-centos",
   "publisher": "cognosys",
   "sku": "secured-silverstripe-on-centos",
   "urn": "cognosys:secured-silverstripe-on-centos:secured-silverstripe-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-simple-invoice-on-centos",
   "publisher": "cognosys",
   "sku": "secured-simple-invoice-on-centos",
   "urn": "cognosys:secured-simple-invoice-on-centos:secured-simple-invoice-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-simple-invoice-on-centos",
   "publisher": "cognosys",
   "sku": "secured-simple-invoice-on-centos",
   "urn": "cognosys:secured-simple-invoice-on-centos:secured-simple-invoice-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-simple-machines-on-centos",
   "publisher": "cognosys",
   "sku": "secured-simple-machines-on-centos",
   "urn": "cognosys:secured-simple-machines-on-centos:secured-simple-machines-on-centos:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-simple-machines-on-centos",
   "publisher": "cognosys",
   "sku": "secured-simple-machines-on-centos",
   "urn": "cognosys:secured-simple-machines-on-centos:secured-simple-machines-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-simple-machines-on-centos",
   "publisher": "cognosys",
   "sku": "secured-simple-machines-on-centos",
   "urn": "cognosys:secured-simple-machines-on-centos:secured-simple-machines-on-centos:1.2.0",
   "version": "1.2.0"
   },
   {
   "offer": "secured-subversion-on-centos",
   "publisher": "cognosys",
   "sku": "new-secured-subversion-on-centos",
   "urn": "cognosys:secured-subversion-on-centos:new-secured-subversion-on-centos:1.2.1",
   "version": "1.2.1"
   },
   {
   "offer": "secured-suitecrm-on-centos",
   "publisher": "cognosys",
   "sku": "secured-suitecrm-on-centos",
   "urn": "cognosys:secured-suitecrm-on-centos:secured-suitecrm-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-test-link-on-centos",
   "publisher": "cognosys",
   "sku": "secured-test-link-on-centos",
   "urn": "cognosys:secured-test-link-on-centos:secured-test-link-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-thinkup-on-centos",
   "publisher": "cognosys",
   "sku": "secured-thinkup-on-centos",
   "urn": "cognosys:secured-thinkup-on-centos:secured-thinkup-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-tikiwikicms-on-centos",
   "publisher": "cognosys",
   "sku": "secured-tikiwikicms-on-centos",
   "urn": "cognosys:secured-tikiwikicms-on-centos:secured-tikiwikicms-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-tiny-tiny-rss-on-centos",
   "publisher": "cognosys",
   "sku": "secured-tiny-tiny-rss-on-centos",
   "urn": "cognosys:secured-tiny-tiny-rss-on-centos:secured-tiny-tiny-rss-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-tomcat-on-centos",
   "publisher": "cognosys",
   "sku": "secured-tomcat-8-on-centos",
   "urn": "cognosys:secured-tomcat-on-centos:secured-tomcat-8-on-centos:1.0.2",
   "version": "1.0.2"
   },
   {
   "offer": "secured-tomcat-on-centos",
   "publisher": "cognosys",
   "sku": "secured-tomcat-8-on-centos",
   "urn": "cognosys:secured-tomcat-on-centos:secured-tomcat-8-on-centos:21.09.24",
   "version": "21.09.24"
   },
   {
   "offer": "secured-trac-on-centos",
   "publisher": "cognosys",
   "sku": "secured-trac-on-centos",
   "urn": "cognosys:secured-trac-on-centos:secured-trac-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-varnish-on-centos",
   "publisher": "cognosys",
   "sku": "hardened-varnish-on-centos-7-3",
   "urn": "cognosys:secured-varnish-on-centos:hardened-varnish-on-centos-7-3:1.0.0",
   "version": "1.0.0"
   },
   {
   "offer": "secured-varnish-on-centos",
   "publisher": "cognosys",
   "sku": "hardened-varnish-on-centos-7-3",
   "urn": "cognosys:secured-varnish-on-centos:hardened-varnish-on-centos-7-3:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "secured-wildfly-on-centos",
   "publisher": "cognosys",
   "sku": "secured-wildfly-on-centos",
   "urn": "cognosys:secured-wildfly-on-centos:secured-wildfly-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-wordpress-on-centos-7-3",
   "publisher": "cognosys",
   "sku": "new-secured-wordpress-on-centos-7-3",
   "urn": "cognosys:secured-wordpress-on-centos-7-3:new-secured-wordpress-on-centos-7-3:1.0.1",
   "version": "1.0.1"
   },
   {
   "offer": "secured-xoops-on-centos",
   "publisher": "cognosys",
   "sku": "secured-xoops-on-centos",
   "urn": "cognosys:secured-xoops-on-centos:secured-xoops-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "secured-zurmo-on-centos",
   "publisher": "cognosys",
   "sku": "secured-zurmo-on-centos",
   "urn": "cognosys:secured-zurmo-on-centos:secured-zurmo-on-centos:1.1.1",
   "version": "1.1.1"
   },
   {
   "offer": "wordpress-with-centos-7-8",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-7-8",
   "urn": "cognosys:wordpress-with-centos-7-8:wordpress-with-centos-7-8:1.2019.1009",
   "version": "1.2019.1009"
   },
   {
   "offer": "wordpress-with-centos-7-9",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-7-9",
   "urn": "cognosys:wordpress-with-centos-7-9:wordpress-with-centos-7-9:1.2019.1009",
   "version": "1.2019.1009"
   },
   {
   "offer": "wordpress-with-centos-75",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-75",
   "urn": "cognosys:wordpress-with-centos-75:wordpress-with-centos-75:21.09.24",
   "version": "21.09.24"
   },
   {
   "offer": "wordpress-with-centos-75-free",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-75-free",
   "urn": "cognosys:wordpress-with-centos-75-free:wordpress-with-centos-75-free:1.2019.1008",
   "version": "1.2019.1008"
   },
   {
   "offer": "wordpress-with-centos-76",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-76",
   "urn": "cognosys:wordpress-with-centos-76:wordpress-with-centos-76:1.2019.1008",
   "version": "1.2019.1008"
   },
   {
   "offer": "wordpress-with-centos-76-free",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-76-free",
   "urn": "cognosys:wordpress-with-centos-76-free:wordpress-with-centos-76-free:1.2019.1008",
   "version": "1.2019.1008"
   },
   {
   "offer": "wordpress-with-centos-77",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-77",
   "urn": "cognosys:wordpress-with-centos-77:wordpress-with-centos-77:1.2019.1008",
   "version": "1.2019.1008"
   },
   {
   "offer": "wordpress-with-centos-77-free",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-77-free",
   "urn": "cognosys:wordpress-with-centos-77-free:wordpress-with-centos-77-free:1.2019.1008",
   "version": "1.2019.1008"
   },
   {
   "offer": "wordpress-with-centos-8-2",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-8-2",
   "urn": "cognosys:wordpress-with-centos-8-2:wordpress-with-centos-8-2:1.2019.1011",
   "version": "1.2019.1011"
   },
   {
   "offer": "wordpress-with-centos-8-2",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-8-2",
   "urn": "cognosys:wordpress-with-centos-8-2:wordpress-with-centos-8-2:1.2019.1012",
   "version": "1.2019.1012"
   },
   {
   "offer": "wordpress-with-centos-8-3",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-8-3",
   "urn": "cognosys:wordpress-with-centos-8-3:wordpress-with-centos-8-3:1.2019.1011",
   "version": "1.2019.1011"
   },
   {
   "offer": "wordpress-with-centos-8-stream",
   "publisher": "cognosys",
   "sku": "wordpress-with-centos-8-stream",
   "urn": "cognosys:wordpress-with-centos-8-stream:wordpress-with-centos-8-stream:1.2019.1011",
   "version": "1.2019.1011"
   }

5. Understand VM sizes
6. VM power states
7. Management tasks

### Notes:

Quickstart: Create a Linux VM

- https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm

Quickstart for Bash in Azure Cloud Shell

- https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart
