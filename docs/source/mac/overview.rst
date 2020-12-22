============
Mac Overview
============

.. contents:: Table of Contents
   :depth: 2

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

- Download and run the installer.

  - Click Continue, Continue, Agree, Install.
  - Enter admin user name and password.
  - Click OK, Close.

- Web Control page opens

  - Enter a name and/or team #, and Passkey. Always use a Passkey.
  - Click Save.

-Done.

After the download, the new V7 software is installed and folding in under 1 minute. Very quick and easy. 
For a more guided installation, please see the Standard Install section.

Standard Installation – Recommended! (All Users)
================================================
This section describes the recommended method for installing the V7 FAH software for individual FAHClient slot(s) on Mac OSX 10.6.x and later. 
A first time installation is assumed. And unless otherwise noted, the default setting for each option is the recommended setting.

Download the V7 Installer package from here (see figure 1). 
The installer includes the new Web Control (client manager) interface software, the new FAHClient (slot manager) software, and the new FAHViewer (viewer) software. 
The optional FAHControl (advanced client manager) is also included.

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX00-download-500x173.png
   :alt: Download-Installer
   :align: center

Figure 1

If you have “Open ‘safe’ files after downloading” selected in Safari, the zip file will be automatically expanded for you (see figure 2). 
Otherwise, double-click the zip file in figure 1 to expand it.

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX01-expand-500x173.png
   :alt: Zip-Expand
   :align: center

Figure 2

Double-click the package to install.

The informational welcome panel is displayed (see figure 3).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX02-welcome-500x355.png
   :alt: Welcome-Panel
   :align: center

Figure 3

Click Continue.

The license agreement is displayed (see figure 4).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX03-license-500x355.png
   :alt: License-Agreement
   :align: center

Figure 4

Please read the agreement, then click Continue.

The option to agree to the license is shown (see figure 5).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX04-license-agree-500x358.png
   :alt: License-Agree
   :align: center

Figure 5

If agreeable, click Agree to continue.

A Select a Destination panel may be displayed. Note that installation is only allowed on the boot disk (see figure 6).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX05a-location-500x355.png
   :alt: Destination-Panel
   :align: center

Figure 6

Select the boot disk, then click Continue.

The standard install panel is displayed (see figure 7).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX05s-standard-install-500x355.png
   :alt: Standard-Install
   :align: center

Figure 7

The option to customize is presented. The default settings are recommend for the standard install.

Click Install to proceed.

The installer prompts for an administrator name and password (see figure 8).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX06-authenticate1.png
   :alt: Authentication
   :align: center

Figure 8

Enter an administrative Name and Password. Click OK to continue.

After a successful installation, this panel is displayed (see figure 9).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/OSX07-success-500x355.png
   :alt: Installation-Success
   :align: center

Figure 9

Click Close.

The installer will quit and the web browser will open to configure the running client.

The Web Control (client manager) interface will start automatically after a few seconds. 
The Web Control page will prompt to configure a FAH user identity (see figure 10).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG15ceConfigID1-500x356.png
   :alt: Web-Control
   :align: center

Figure 10

Click the Configure an Identity button unless choosing to fold Anonymously.

The Web Control Identity tab is displayed (see figure 11).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG16ceEnterID1-500x318.png
   :alt: Change-ID
   :align: center

Figure 11

Enter a FAH user Name, Team #, and Passkey as needed.  Always use a Passkey.

Note: Using a Passkey adds an extra level of security, and is also a requirement to receiveQuick Return Bonus points.

Click Save to continue.

The Web Control Home tab is displayed (see figure 12).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG17ceWebControl1-500x393.png
   :alt: Web-Home
   :align: center

Figure 12

V7 software is now installed and folding.

Please read the V7 Introduction page for basic information and further explanations of the new client features.

See also the FAHControl, FAHClient, and FAHViewer documents for more information about setup and customization options.

While the default options are typically the recommended options, see the ConfigurationFAQ for additional setup options.