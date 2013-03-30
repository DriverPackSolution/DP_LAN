Setting up Intel(R) 10GbE Network Connection Drivers for Micorsoft* Windows* PE
===============================================================================
To set up network drivers for Microsoft* Windows* PE, you must import files from the Intel(R) Network Connections Software CD to the Windows PE image. Follow the directions for your operating system.

Intel(R) 10GbE Network Connections Drivers are not supported on Microsoft* Windows* XP.



32-bit Microsoft Windows PE v1.6
================================

1. Create a temporary directory (for example, c:\temp\winpe).

2. Copy all files from the PROXGB\Win32\NDIS5x directory to the temporary directory. Do NOT copy the INF files to this directory.

3. Extract the .INF files from PROXGB\Win32\NDIS5x\WinPE\*.zip to the temporary directory.

4. Use the  /inf option of the drvinst.exe tool to import the drivers into the WinPE image. For example, use the following command:

   drvinst /inf:c:\temp\winpe\ixn5132.inf /inject:c:\mounted_winpe

The syntax for the drvinst.exe tool is as follow:

   drvinst /inf:<path> /inject:<%WINPEDIR%>

    /inf:<path> specifies that you want to import an .inf package, where <path> is the path to the .inf file. 
    /inject:<%WINPEDIR%> specifies the action drvinst should take, where <%WINPEDIR%> is the path to the Windows PE image directory.

Please see your Microsoft Windows PE documentation or the Microsoft website for more information on using drvinst.exe

x64 Microsoft Windows PE v1.6
=============================

1. Create a temporary directory (for example, c:\temp\winpe).

2. Copy all files from the PROXGB\Winx64\NDIS5x directory to the temporary directory. Do NOT copy the INF files to this directory.

3. Extract the .INF files from PROXGB\Winx64\NDIS5x\WinPE\*.zip to the temporary directory.

4. Use the  /inf option of the drvinst.exe tool to import the drives into the WinPE image. For example, use the following command:

   drvinst /inf:c:\temp\winpe\ixn51x64.inf /inject:c:\mounted_winpe

The syntax for the drvinst.exe tool is as follow:

   drvinst /inf:<path> /inject:<%WINPEDIR%>

    /inf:<path> specifies that you want to import an .inf package, where <path> is the path to the .inf file. 
    /inject:<%WINPEDIR%> specifies the action drvinst should take, where <%WINPEDIR%> is the path to the Windows PE image directory.

Please see your Microsoft Windows PE documentation or the Microsoft website for more information on using drvinst.exe



32-bit Microsoft Windows PE V2
==============================

1. Create a temporary directory (for example, c:\temp\winpe).

2. Copy all files from the PROXGB\Win32\NDIS61 directory to the temporary directory. Do NOT copy the INF files to this directory.

3. Extract the .INF files from PROXGB\Win32\NDIS61\WinPE\*.zip to the temporary directory.

4. Use the  /inf option of the peimg.exe tool to import the drives into the mounted WinPE image. For example, use the following command:

     peimg /inf=c:\temp\winpe\ixn6032.inf c:\mounted_winpe

The syntax for the peimg.exe tool is as follow:

  peimg /inf=<path> <%WINPEDIR%>

    /inf=<path> specifies that you want to import an .inf package, where <path> is the path to the .inf file.
    <%WINPEDIR%> specifies the path to the directory where you have mounted your Windows PE image.

Please see your Microsoft Windows PE documentation or the Microsoft website for more information on using peimg.exe

x64 Microsoft Windows PE V2
===========================

1. Create a temporary directory (for example, c:\temp\winpe).

2. Copy all files from the PROXGB\Winx64\NDIS61 directory to the temporary directory. Do NOT copy the INF files to this directory.

3. Extract the .INF files from PROXGB\Winx64\NDIS61\WinPE\*.zip to the temporary directory.

4. Use the  /inf option of the peimg.exe tool to import the drives into the mounted WinPE image. For example, use the following command:

     peimg /inf=c:\temp\winpe\ixn60x64.inf c:\mounted_winpe

The syntax for the peimg.exe tool is as follow:

  peimg /inf=<path> <%WINPEDIR%>

    /inf=<path> specifies that you want to import an .inf package, where <path> is the path to the .inf file.
    <%WINPEDIR%> specifies the path to the directory where you have mounted your Windows PE image.

Please see your Microsoft Windows PE documentation or the Microsoft website for more information on using peimg.exe



32-bit Microsoft Windows PE V3
==============================

1. Create a temporary directory (for example, c:\temp\winpe).

2. Copy all files from the PROXGB\Win32\NDIS62 directory to the temporary directory. Do NOT copy the INF files to this directory.

3. Extract the .INF files from PROXGB\Win32\NDIS62\WinPE\*.zip to the temporary directory.

4. Use the  /Add-Driver option of the DISM.exe tool to import the drives into the image. For example, use the following command:

     	Dism /image:C:\mounted_winpe /Add-Driver /driver:c:\temp\winpe\ixn6232.inf

The syntax for the dism.exe tool is as follow:

  dism /image:<%WINPEDIR%> /Add-Driver /driver:<path>  

    /image:<%WINPEDIR%> specifies the path to the directory where you have mounted your Windows PE image.
    /Add-Driver specifices the action dism should take.
    /driver:<path> specifies the path to the driver inf file.

Please see your Microsoft Windows PE documentation or the Microsoft website for more information on using dism.exe

x64 Microsoft Windows PE V3
===========================

1. Create a temporary directory (for example, c:\temp\winpe).

2. Copy all files from the PROXGB\Winx64\NDIS62 directory to the temporary directory. Do NOT copy the INF files to this directory.

3. Extract the .INF files from PROXGB\Winx64\NDIS62\WinPE\*.zip to the temporary directory.

4. Use the  /Add-Driver option of the DISM.exe tool to import the drives into the image. For example, use the following command:

     	Dism /image:C:\mounted_winpe /Add-Driver /driver:c:\temp\winpe\ixn62x64.inf

The syntax for the dism.exe tool is as follow:

  dism /image:<%WINPEDIR%> /Add-Driver /driver:<path>  

    /image:<%WINPEDIR%> specifies the path to the directory where you have mounted your Windows PE image.
    /Add-Driver specifices the action dism should take.
    /driver:<path> specifies the path to the driver inf file.

Please see your Microsoft Windows PE documentation or the Microsoft website for more information on using dism.exe



Copyright (C) 2009 Intel Corporation.  All rights reserved.
Intel is a trademark or registered trademark of Intel Corporation or its subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.
