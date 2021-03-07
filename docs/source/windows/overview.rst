================
Windows Overview
================

.. contents:: Table of Contents
   :local:

Introduction to V7
==================
The new Folding\@home (FAH) software is configured, controlled, and monitored through a new simpler graphical interface named Web Control. 
This new web browser based application has incorporated many new features, including client monitoring and configuration of all FAH clients. 
Web Control is now the recommended interface for all FAH types (Single core CPU, Multi-core CPU, GPU), 
replacing both the Systray and the Console versions of FAH. The more advanced FAHControl application is also available.

New Terminology
===============
The V7 software really changes the concept of how people interact with FAH. 
And with new concepts come new or updated terms to describe those concepts. 
Learning new references is part of the process for change and improvement.

- Web Control – This is the new simpler graphical interface (front-end). 
  Web Control will configure and monitor one or more FAHClient slots through an easy to use web page. This is the default control program.
- FAHControl – This is an alternate new graphical interface (advanced front-end). 
  FAHControl will configure and monitor one or more FAHClient (slots), on one or more computers. This more advanced interface is optional.
- FAHClient – This is the (back-end) client software managed by FAHControl and typically runs behind the scene. 
  This is a truly unified client (slot) manager. 
  FAHClient starts one or multiple instances of a Fahcore and manages the work assignments for each of these client “slots.”
- FAHSlot – aka “slot” – Each Fahcore and the data associated with it is called a slot. 
  For example, one FAHSlot can be associated with a GPU and another slot associated with the CPU. 
  Each folding slot can download, process, and upload results independently. 
  The FAHClient manages each slot, and FAHControl monitors and displays their progress independently.
- FAHViewer – This is the new and fully functional work unit viewer. 
  FAHViewer is modeled after the very popular PS3 viewer, and continues to offer the many rendering options, 
  ball and stick, space fill, zoom, rotation, etc., and adds snapshot capture and cycling to show folding in action.

See also the `FAHControl <https://foldingathome.org/projects/FAHClient/wiki/FahControl>`_, 
`FAHClient <https://fah.stanford.edu/projects/FAHClient/wiki/ClientUserGuide>`_, 
and `FAHViewer <https://fah.stanford.edu/projects/FAHClient/wiki/FahViewer>`_ documents for more information about setup and customization options.

What is new in V7?
==================
We are pleased to say that everything is new in this version, using completely new software coding from the ground up. 
Our goal is to include the best features from the previous clients, make improvements where possible, discard what was no longer needed, 
then add new features like the quick start Express mode installer, the new FAHViewer, and the new unified interface. 
V7 has all of these and more, making installation and configuration much simpler and faster for new users, while continuing to support advanced options.

Note: There are too many updated and new features to list in an Installation Guide, so this section only covers What’s New when installing V7 software. 
Please read the V7 Introduction page for basic information and explanations of the new client features.

Quick Start
===========
This section describes how to get started folding quickly with the new V7 software and the default FAHClient slot(s).

- `Download <https://download.foldingathome.org/>`_ and run the installer.
- Click Yes, Next, I Agree, Next, Finish.
- Enter a name and/or team #, and Passkey.  Always use a Passkey.
- Click Save.
- Done.

After the download, the new V7 software is installed and folding in under 1 minute. Very quick and easy. 
For a more guided installation, please see the Express Install or Custom Setup sections.

Express Installation – Recommended! (All Users)
===============================================
This section describes the recommended method for installing the V7 FAH software for individual FAHClient slot(s) on Windows XP and newer. 
A first time installation is assumed. And unless otherwise noted, the default setting for each option is the recommended setting.

Download the V7 Installer from here (see figure 1). 
The installer includes the new Web Control (client manager) interface software, the new FAHClient (slot manager) software, and the new FAHViewer (viewer) software. 
The optional FAHClient (advanced client manager) is also included.

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG00FCInstall1.png
   :alt: FAH-Installer
   :align: center

.. rst-class:: center

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

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG04eFCInstall7-500x389.png
   :alt: Installer-Mode
   :align: center

Figure 5

Click Next to continue the Express (Recommended) installation.

Note: Express Install will automatically install one or more FAHClient slots to match the computer hardware detected. 
If multiple CPU cores are detected, an multicore CPU slot is installed, otherwise a single core CPU slot is installed as the fall back option. 
If one or more GPUs are detected, one or more GPU slots are also installed automatically. 
If neither multicores or GPU are detected, a single core CPU slot is installed by default. 
The separate SMP and Uniprocessor slot types are now combined and known as a CPU slot, supporting one to many CPU cores.

Please wait while the installation finishes (see figure 6).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG11ceFCInstall7-500x389.png
   :alt: Installation
   :align: center

Figure 6

V7 installation is almost complete (see figure 7).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG12ceFCFinish-500x389.png
   :alt: Installation-Finish
   :align: center

Figure 7

Note: Do not uncheck the box to Start Folding\@home so the software will start automatically with Windows. 
If unchecked, FAHClient will need to be started manually each time.

Click Finish.

A prompt from Windows Firewall or another security software may be displayed (see figure 8).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG14ceFCInstall7-500x358.png
   :alt: Windows-Security
   :align: center

Figure 8

If prompted, select Unblock or Allow Access for V7 software to connect to the internet.

The Web Control (client manager) interface will start automatically after a few seconds. 
The Web Control page will prompt to configure a FAH user identity (see figure 9).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG15ceConfigID1-500x356.png
   :alt: Web-Control
   :align: center

Figure 9

Click the Set up an Identity radio button unless choosing to fold Anonymously.

Click the Start Folding button after making a selection.

The Web Control Change Identity window is displayed (see figure 10).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG16ceEnterID1-500x318.png
   :alt: Change-ID
   :align: center

Figure 10

Enter a FAH user Name, Team #, and Passkey as needed. Always use a Passkey.

Note: Using a Passkey adds an extra level of security, and is also a requirement to receiveQuick Return Bonus points.

Click Save to continue.

The Web Control Home tab is displayed (see figure 11).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG17ceWebControl1-500x393.png
   :alt: Web-Home
   :align: center

Figure 11

V7 software is now installed and folding.

Note: Move the Power Slider to Full for maximum production.

Please read the V7 Introduction page for basic information and further explanations of the new client features.

See also the FAHControl (client manager), FAHClient (slot), 
and FAHViewer (viewer) documents for more information about setup and customization options.

While the default options are typically the recommended options, see the ConfigurationFAQ for additional setup options.