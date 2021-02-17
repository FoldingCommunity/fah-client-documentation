======================
GUI Based Installation
======================

.. contents::
   :local:


GUI Installation Steps
----------------------

This section describes the recommended method for installing the V7 FAH software for an individual client slot using a software package in Linux. A first time installation is assumed. And unless otherwised noted, the default setting for each option is the recommended setting.

Select the appropriate V7 package for your Linux distribution from the V7 download page. (see figure 1). There are separate installation packages for the new FAHControl (client manager) interface software, the new FAHClient (slot manager) software, and the new FAHViewer (viewer) software. FAHClient is required, FAHControl is recommended, FAHViewer is optional.


.. image:: overview_linux_figures/figure1.png

Figure 1

Click the link for a matching operating system to start the software installation, or click the See all downloads link, and select the appropriate operating system from the full list.

Linux will ask how to handle the package file download (see figure 2).


.. image:: overview_linux_figures/figure2.1.png
.. image:: overview_linux_figures/figure2.2.png

Debian / Mint / Ubuntu <– Figure 2 –> Fedora / CentOS / Red Hat

When prompted, click OK to open the package installer.

Note: Some versions of Linux do not have a package installer program listed to open the file directly. The only option is to save the file, and then open the file in the Downloads folder with the software manager. The process is very similar and the rest of the setup is the same.

The Package Installer is displayed (see figure 3).

.. image:: overview_linux_figures/figure3.1.png
.. image:: overview_linux_figures/figure3.2.png

Debian / Mint / Ubuntu <– Figure 3 –> Fedora / CentOS / Red Hat

Click the Install Package or Apply button to continue the installation.

Enter an administrator password when prompted (see figure 4).

.. image:: overview_linux_figures/figure4.1.png
.. image:: overview_linux_figures/figure4.2.png

Debian / Mint / Ubuntu <– Figure 4 –> Fedora / CentOS / Red Hat

The Package Installer prompts for initial setup information in Debian / Ubuntu installs only (see figure 5).

Note: Fedora / Red Hat .rpm packages do not support prompting for setup information. Instead, the client is set to paused so initial setup information may be entered through the FAHControl interface. However, there is a 5 minute time limit on this initial pause.  After that, the client will start and download work using the current default settings.

.. image:: overview_linux_figures/figure5.png


Additional configuration changes are optional and may be skipped. If no changes are made, the client will run with these default settings:

- User Name: Anonymous
- Team Number: 0
- Passkey: None
- Power: Medium
- Start: Automatic


Or enter a Donor Name, Team number, and/or Passkey number. Entering a passkey is recommended but not required. However, a passkey is required to participate in the Quick Return Bonus points system.  For maximum production, change the Power resource setting from medium to ALL.

Note: DO NOT uncheck to box to start the FAHClient automatically.  Starting the FAHClient manually is considered an expert only feature.

Note: Express Installation (ALL) automatically installs a single client slot to match the computer hardware detected. If multiple CPU cores are detected, a multi-core CPU slot is installed. If not, then a single core CPU slot is installed as the fall back option. A GPU slot option is also supported in the Linux client.

Click Forward to continue.

The Package Installer shows installation progress (see figure 6).

.. image:: overview_linux_figures/figure6.1.png
.. image:: overview_linux_figures/figure6.2.png

Debian / Mint / Ubuntu <– Figure 6 –> Fedora / CentOS / Red Hat

Finishing the install will take another minute or two.

Installation is complete (see figure 7).

.. image:: overview_linux_figures/figure7.1.png
.. image:: overview_linux_figures/figure7.2.png

Debian / Mint / Ubuntu <– Figure 7 –> Fedora / CentOS / Red Hat

Click the Close button. The V7 software is installed and running as a service.

Repeat steps 1 – 7 with the FAHControl package, and optionally, the FAHViewer package.

Settings may be updated and progress can be monitored in FAHControl (see figure 8).

.. image:: overview_linux_figures/figure8.1.png
.. image:: overview_linux_figures/figure8.2.png

Debian / Mint / Ubuntu <– Figure 8 –> Fedora / CentOS / Red Hat

The FAHControl application launches.

This is the FAHControl (client manager) interface . The client should display ONLINE and Running (see figure 9).

.. image:: overview_linux_figures/figure9.png

V7 software is now installed and folding.

Please read the V7 Introduction page for basic information and further explanations of the new client features.

See also the FAHControl (client manager), FAHClient (slot), and FAHViewer (viewer) documents for more information about setup and customization options.

While the default options are typically the recommended options, see the Configuration FAQ for additional setup options.
