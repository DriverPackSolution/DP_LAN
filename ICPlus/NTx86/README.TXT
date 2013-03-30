
                IC Plus IP1000 Family Gigabit Ethernet Adapter
                         Windows NDIS6 driver 


Contents:
---------

1. File Description
2. Driver Installation for Windows Vista 
3. Parameters Description


1. File Description
-------------------

Filename              Description
=================     =====================================================
README.TXT            Presents a summary of the contents for Windows NDIS
                      driver installation.

NETIPGD.INF           Windows installation INFormation file for install

IPGDND60.SYS          Windows Vista NDIS 6.0 driver

2. Driver Installation for Windows Vista 
------------------------------------------------

    The Windows installation floppy or CD is needed to complete this
    installation.

    Adapter Installation Procedure
    --------------------------------------------

    a. Make sure your computer is power-off.

    b. Plug the adapter into one PCI 33MHz slot of your computer.

    c. Turn on the power. 

    Install and/or Update driver from diskette
    ------------------------------------------
    The following steps can help you install or update the driver to
    the one in the Adapter Drivers Diskette/CD-ROM.

     a. Open Control Panel, double click "Device Manager" icon to open Device Manager
        Window.

     b. In Other device category, right-click 

  		Ethernet Controller

        and select "Update Driver Software".

     c. Browse to the direcotry with the device driver and click on Next.

     d. The wizard will automatically search the device driver in the browsed directory, 
        and install the driver.

3. Parameter Description
------------------------

     a. Open Control Panel, double click "Device Manager" icon to open Device Manager
        Window.

     b. In Network Adapters category, right-click 

  		IC Plus IP1000 Family Gigabit Ethernet Adapter

        and select "Property".

     c. In Advanced, following parameters can be used to configure the adapter.


	Connection Type      Specify the connection type for the adapter.
                         Default: Auto-Sense

	Network Address      Set the Ethernet address for your adapter. 
                         It is not recommended to use this. 
                         Default: read address from adapter ROM.

	Receive Buffers	     Set the number of Receive Buffers Descriptors
                         Default : 96

	Transmit BUffers     Set the number of Transmit Buffers Descriptors
                         Default : 96

                            
      
	   						
 