=======================================================
Multi-client Installation - Adding Slots (Expert Users)
=======================================================

This section describes how to add one or more additional FAHClient slots for Windows XP and newer using the FAHControl interface. 
When mixing GPU and CPU slots, the setup is quicker and easier to use the V7 installer to add both at the same time. 
Even after a hardware upgrade, uninstalling and reinstalling is often easier and faster for adding slots for the new hardware.

In the rare event the installer does not add a slot, the procedure to add a slot manually is shown below.

This procedure assumes expert user knowledge of Windows and V7 Folding\@home software, 
and at least one other working and running FAHClient slot. 
Unless otherwise noted, the default setting for each option is the recommended setting.

Note: Additional slots can be added manually by editing the FAHClient configuration file. 
However, this is very risky as incorrect settings or typing mistakes may cause the current work unit to abort, the client to crash, 
or future points to be credited to someone else.

The recommended procedure for adding additional FAHClient slots is through the FAHControl Configuration settings. 
Right-click the FAH system tray icon to open Advanced Control (see figure 1).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG18TrayIcon1.png
   :alt: Advanced-Control
   :align: center

Figure 1

The FAHControl interface is displayed (see figure 2).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG19FAHControl-500x444.png
   :alt: FAHControl-Interface
   :align: center

Figure 2

Click the Configure button (on toolbar).

The Configure window and Identity tab are displayed by default (see figure 3).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG20IdentityTab-500x404.png
   :alt: Configuration
   :align: center

Figure 3

Select the Slots tab.

The current Folding Slots are listed (see figure 4).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG21SlotsTab-500x277.png
   :alt: Folding-Slots
   :align: center

Figure 4

Click the Add button.

The Configure Folding Slots screen is displayed (see figure 5).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG22ConfigSlots-500x609.png
   :alt: Configure-Slots
   :align: center

Figure 5

Select the slot type to be added, CPU or GPU. 
When adding a CPU slot, please select the correct number of processing cores to match the computer. 
When adding a GPU slot, the recommended setting is -1 as the client will autodetect the correct GPU device number.

Click OK to continue. The Slots tab is displayed again, with the new FAHClient slot in the list (see figure 6).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG23GPUSlot-500x291.png
   :alt: Slot-List
   :align: center

Figure 6

Repeat as needed to add additional new FAHClient slots, or click Save to finish the configuration and return to the main FAHControl screen.

Note: The new FAHClient slots will use the same performance settings (CPU percentage, Checkpoint frequency, etc.) 
as defined on the Advanced Tab of the Configuration settings.

The new slot will download a new work unit and starting folding automatically.

Exit the FAHControl application when done.

