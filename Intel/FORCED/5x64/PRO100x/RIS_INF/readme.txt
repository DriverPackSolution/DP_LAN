Setting up Intel(R) PRO/100 Drivers for RIS Installation
======================================================
To set up network drivers for RIS installation, you must copy files from the Intel(R) Network Connections Software CD to the RIS image [IMAGE_ROOT]. Follow the directions for your operating system.


Microsoft Windows XP and  Microsoft* Windows Server* 2003 (32-bit)
==================================================================

1. Create an [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory if one does not already exist.

2. Copy all files from the PRO100\WIN32\NDIS5x directory to the [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory.

3. Make the following changes to the .SIF file that is used for this image installation (located in the [IMAGE_ROOT]\I386\Templates directory): 

[Unattended]
OemPreinstall = yes
OemPnpDriversPath = \Drivers\Nic 
 
4. Copy all .SYS files from PRO100\WIN32\NDIS5x directory to the [IMAGE_ROOT]\i386 directory. Do NOT copy the INF files to this directory.

5. Extract the .INF file from PRO100\WIN32\NDIS5x\RIS_INF\E100B325.ZIP to the [IMAGE_ROOT]\i386 directory.

6. Restart the Remote Installation Service.

7. Follow the rest of the Microsoft instructions for adding a new network driver to the RIS installation.


Microsoft Windows XP 64-bit Edition and 
Microsoft Windows Server 2003, 64-bit Edition
=============================================

1. Create an [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory if one does not already exist.

2. Copy all files from the PRO100\WIN64\NDIS5x directory to the [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory.

3. Make the following changes to the .SIF file that is used for this image installation (located in the [IMAGE_ROOT]\ia64\Templates directory): 

[Unattended]
OemPreinstall = yes
OemPnpDriversPath = \Drivers\Nic 
 
4. Copy all .SYS files from the PRO100\WIN64\NDIS5x directory to the [IMAGE_ROOT]\ia64 directory. Do NOT copy the INF files to this directory.

5. Extract the .INF file from PRO100\WIN64\NDIS5x\RIS_INF\E100B645.ZIP to the [IMAGE_ROOT]\ia64 directory. 

6. Restart the Remote Installation Service. 

7. Follow the rest of the Microsoft instructions for adding a new network driver to the RIS installation.


Microsoft Windows XP x64 and Microsoft Windows Server 2003 x64
==============================================================

1. Create an [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory if one does not already exist.

2. Copy all files from the PRO100\WINX64\NDIS5x directory to the [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory.

3. Make the following changes to the .SIF file that is used for this image installation (located in the [IMAGE_ROOT]\amd64\Templates directory): 

[Unattended]
OemPreinstall = yes
OemPnpDriversPath = \Drivers\Nic 
 
4. Copy all .SYS files from the PRO100\WINX64\NDIS5x directory to the [IMAGE_ROOT]\amd64 directory. Do NOT copy the INF files to this directory.

5. Extract the .INF file from PRO100\WINX64\NDIS5x\RIS_INF\EFE5B32E.ZIP to the [IMAGE_ROOT]\amd64 directory.

6. Restart the Remote Installation Service. 

7. Follow the rest of the Microsoft instructions for adding a new network driver to the RIS installation.



Copyright (C) 2009 Intel Corporation.  All rights reserved.
Intel is a trademark or registered trademark of Intel Corporation or its subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.
