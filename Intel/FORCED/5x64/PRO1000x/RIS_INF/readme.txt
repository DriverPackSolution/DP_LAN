Setting up Intel(R) Gigabit Network Connection Drivers for RIS Installation
===========================================================================
To set up network drivers for RIS installation, you must copy files from the Intel(R) Network Connections Software CD to the RIS image [IMAGE_ROOT]. Follow the directions for your operating system.

Microsoft Windows XP and  Microsoft* Windows Server* 2003 (32-bit)
==================================================================

1. Create an [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory if one does not already exist.

2. Copy all files from the PRO1000\Win32\NDIS5x directory to the [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory.

3. Make the following changes to the .SIF file that is used for this image installation (located in the [IMAGE_ROOT]\I386\Templates directory): 

[Unattended]
OemPreinstall = yes
OemPnpDriversPath = \Drivers\Nic 
 
4. Copy all .SYS files from PRO1000\Win32\NDIS5x directory to the [IMAGE_ROOT]\i386 directory. Do NOT copy the INF files to this directory.

5. Delete E1000325.PNF, E1E5132.PNF, E1Q5132.PNF, and E1Y5132.PNF (if present) from the [IMAGE_ROOT]\i386 directory. 

6. Extract the .INF files from PRO1000\Win32\NDIS5x\RIS_INF\E1000325.ZIP, E1E5132.zip, E1Q5132.ZIP, and E1Y5132.ZIP to the [IMAGE_ROOT]\i386 directory.

7. Restart the Remote Installation Service.

8. Follow the rest of the Microsoft instructions for adding a new network driver to the RIS installation.


Microsoft Windows Server 2003, 64-bit Edition
=============================================

1. Create an [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory if one does not already exist.

2. Copy all files from the PRO1000\Win64\NDIS5x directory to the [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory.

3. Make the following changes to the .SIF file that is used for this image installation (located in the [IMAGE_ROOT]\ia64\Templates directory): 

[Unattended]
OemPreinstall = yes
OemPnpDriversPath = \Drivers\Nic 
 
4. Copy all .SYS files from the PRO1000\Win64\NDIS5x directory to the [IMAGE_ROOT]\ia64 directory. Do NOT copy the INF files to this directory.

5. Delete E1000645.PNF, E1E5164.PNF and E1Q5164.PNF (if present) from the [IMAGE_ROOT]\ia64 directory. 

6. Extract the .INF file from PRO1000\Win64\NDIS5x\RIS_INF\E1000645.ZIP, E1E5164.ZIP and E1Q5164.ZIP to the [IMAGE_ROOT]\ia64 directory. 

7. Restart the Remote Installation Service. 

8. Follow the rest of the Microsoft instructions for adding a new network driver to the RIS installation.

Known Issues: 
RIS installations are not supported on Itanium(R)-based systems using PCIe quad port Intel(R) Server Adapters.



Microsoft Windows XP x64 and Microsoft Windows Server 2003 x64
==============================================================

1. Create an [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory if one does not already exist.

2. Copy all files from the PRO1000\Winx64\NDIS5x directory to the [IMAGE_ROOT]\$oem$\$1\Drivers\NIC directory.

3. Make the following changes to the .SIF file that is used for this image installation (located in the [IMAGE_ROOT]\amd64\Templates directory): 

[Unattended]
OemPreinstall = yes
OemPnpDriversPath = \Drivers\Nic 
 
4. Copy all .SYS files from the PRO1000\Winx64\NDIS5x directory to the [IMAGE_ROOT]\amd64 directory. Do NOT copy the INF files to this directory.

5. Delete E1G5132E.PNF, E1E5132E.PNF, E1Q51X64.PNF and E1Y51X64.PNF (if present) from the [IMAGE_ROOT]\amd64 directory. 

6. Extract the .INF files from PRO1000\Winx64\NDIS5x\RIS_INF\E1G5132E.ZIP, E1E5132E.ZIP, E1Q51X64.ZIP, and E1Y51X64.ZIP to the [IMAGE_ROOT]\amd64 directory.

7. Restart the Remote Installation Service. 

8. Follow the rest of the Microsoft instructions for adding a new network driver to the RIS installation.



Copyright (C) 2009 Intel Corporation.  All rights reserved.
Intel is a trademark or registered trademark of Intel Corporation or its subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.
