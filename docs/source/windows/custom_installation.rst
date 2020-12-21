====================================
Custom Installation (Advanced Users)
====================================

Custom Installation – Optional (Advanced Users)
===============================================
This section describes V7 FAH custom options available when installing FAHClient slot(s) on Windows XP and newer. 
This procedure assumes advanced knowledge of Windows and V7 Folding\@home software. 
A first time installation is assumed, and unless otherwise noted, the default setting for each option is the recommended setting.

Note: To install a V7 FAHClient slot to run as a service (an option a bit later in the setup), 
the Windows XP user account running the installer must have Administrator privileges. 
In Windows Vista and newer, the installer must be opened with the Run As Administrator option. 
Do this by right-clicking on the installer icon and then click Run as Administrator. 
If prompted for an administrator password or confirmation, enter the password or provide confirmation. 
If a service install is the goal, this would be a good time to change to a user account with Administrative rights in XP, 
or to use the Run As option in Vista/7/8.

Note: Windows Vista, Windows 7/8, and newer do not support running a GPU FAHClient slot as a service (a Microsoft security limitation).

Download the V7 Installer from here (see figure 1). The installer includes the new simpler Web Control (client manager), 
the new FAHClient (slot) software, and the new FAHViewer (viewer) software.  
V7 also includes the optional FAHControl (advanced client manager) interface software.

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG00FCInstall1.png
   :alt: FAH-Installer
   :align: center

Figure 1

Double-click the Installer icon to start the software installation.

A security warning prompt may be displayed (see figure 2).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG01FCInstall7.png
   :alt: Security-Warning
   :align: center

Figure 2

If prompted, click Run or click Yes to acknowledge the warning and continue the installation.

The welcome screen is displayed (see figure 3).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG02FCInstall7-500x389.png
   :alt: Welcome-Screen
   :align: center

Figure 3

Click Next to continue the installation.

Read the License Agreement (see figure 4).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG03FCInstall7-500x389.png
   :alt: License-Agreement
   :align: center

Figure 4

If agreeable, click I Agree to continue.

The Installer Mode option screen is displayed (see figure 5).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG04cFCInstall7-500x389.png
   :alt: Installer-Mode
   :align: center

Figure 5

Select the Custom Install (Advanced) option as pictured. Click Next to proceed.

The Choose Users screen is shown (see figure 6).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG05cFCInstall7-500x389.png
   :alt: Choose-User
   :align: center

Figure 6

Select an option for which users will run V7 software. Install just for me is recommended. Click Next.

The client location screen is shown (see figure 7).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG06cFCInstall7-500x389.png
   :alt: Client-Location
   :align: center

Figure 7

An alternate destination folder may be entered, but this default is recommended. Click Nextto continue.

The client data files location screen is shown. The current Windows account name will appear in place of [User_Name] (see figure 8).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG07cFCInstall7-500x389.png
   :alt: Client-Data-Loc
   :align: center

Figure 8

An alternate data directory folder may be entered for V7 configuration and data files location. 
However, this is the recommended default. Click Next.

The Start Software options are displayed (see figure 9). These are very important for determining how the FAHClient will start. 
It also selects if and how the FAHClient slots are controlled and monitored by FAHControl on this computer.

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG08cFCStartupOpts-500x389.png
   :alt: Start-Software
   :align: center

Figure 9

How would you like to start the folding client?

The options pictured in figure 9 match the default settings used in the Express install, and are the recommended settings. 
Or select custom startup options below.

- The first option sets the FAHClient slot(s) to start at Windows login. 
  Any FAHClient slot is only visible in the Web Control or Advanced Control interfaces.
- The second option sets the FAHClient slot to run as a service, and is only visible in the FAHControl interface. 
  Service Mode is not available to GPU clients in Windows Vista and Windows 7/8 (a Microsoft security limitation).
- The third option is used to start the FAHClient manually from a shortcut.
- This check box enables the Folding\@home screensaver. 
  It is a recommended option, but may use some computer resources that might otherwise be used for folding, depending on the system configuration.

Note: The installer will automatically install one or more FAHClient slots to match the computer hardware detected. 
If multiple CPU cores are detected, an a multi-core CPU slot is installed, otherwise a single core CPU slot is installed as the fall back option. 
If one or more GPUs are detected, one or more GPU slots are also installed automatically. 
If neither multicores or GPU are detected, a single CPU slot is installed by default.

Note: This section describes how to add an additional slot: Multi-client Installation – Adding slots

Click Install to continue.

Please wait while Folding\@home is finishing the installation (see figure 10).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG11ceFCInstall7-500x389.png
   :alt: Installation
   :align: center

Figure 10

V7 client installation is almost complete (see figure 11).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG12ceFCFinish-500x389.png
   :alt: Installation-Finish
   :align: center

Figure 11

Note: Do not uncheck the box to Start Folding\@home so the software will start automatically with Windows. 
If unchecked, FAHClient will need to be started manually each time.

Click Finish.

A prompt from Windows Firewall or another security software may be displayed (see figure 12).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG14ceFCInstall7-500x358.png
   :alt: Windows-Security
   :align: center

Figure 12

If prompted, select unblock or Allow access for V7 software to connect to the internet.

The Web Control (client manager) interface will start automatically after a few seconds. 
The Web Control page will prompt to configure a FAH user identity (see figure 13).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG15ceConfigID1-500x356.png
   :alt: Web-Control
   :align: center

Figure 13

Click the Set up an Identity radio button unless choosing to fold Anonymously.

Click the Start Folding button after making a selection.

The Web Control Change Identity window is displayed(see figure 14).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG16ceEnterID1-500x318.png
   :alt: Change-ID
   :align: center

Figure 14

Enter a FAH user Name, Team #, and Passkey as needed. Always use a Passkey.

Note: Using a Passkey adds an extra level of security, and is also a requirement to receiveQuick Return Bonus points.

Click Save to continue.

The Web Control Home tab is displayed (see figure 15).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG17ceWebControl1-500x393.png
   :alt: Web-Home
   :align: center

Figure 15

V7 software is now installed and folding.

Note: Move the Power Slider to Full for maximum production.

Please read the V7 Introduction page for basic information and further explanations of the new client features.

See also the FAHControl (client manager), FAHClient (slot), 
and FAHViewer (viewer) documents for more information about setup and customization options.

While the default options are typically the recommended options, see the ConfigurationFAQ for additional setup options.