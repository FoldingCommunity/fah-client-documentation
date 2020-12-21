==============================
Manual Installation (Advanced)
==============================

Manual Installation – Optional (Advanced)
------------------------------------------

Here are the basic command-line instructions to install and run the V7 Folding@home software.

Open the Terminal / Console application. Depending on the Linux distribution (Ubuntu, Fedora, etc.), OS version, and desktop engine (KDE, GNOME, Unity, etc.) the Terminal / Console application may be found in a variety of locations. It is typically located under Accessories or System Tools.  This is not for Linux running in Terminal mode (no GUI).

Type each command exactly as it appears, or cut and paste directly from this guide.

Note: The installation commands shown include options to continue even when exact dependencies are not met. The V7 software is rather generic and works with most, if not all, version of the various libraries.

Terminal installation for Debian / Mint / Ubuntu
-------------------------------------------------

Download the installation package files; 64-bit versions shown. If using an i386/i686 32-bit OS version, download those files as appropriate from the client download page::

        wget https://download.foldingathome.org/releases/public/release/fahclient/debian-testing-64bit/v7.4/fahclient_7.4.4_amd64.deb
        wget https://download.foldingathome.org/releases/public/release/fahcontrol/debian-testing-64bit/v7.4/fahcontrol_7.4.4-1_all.deb
        wget https://download.foldingathome.org/releases/public/release/fahviewer/debian-testing-64bit/v7.4/fahviewer_7.4.4_amd64.deb

Install the FAHClient::

        sudo dpkg -i --force-depends fahclient_7.4.4_amd64.deb

The package will prompt for initial setup information, user name, etc. Enter information or change as needed, and click OK.

Install the FAHControl application.  Root privileges are required.  FAHControl will show “offline” or “connecting” status until the FAHClient is running, either started automatically (strongly recommended) or started manually::

        sudo dpkg -i --force-depends fahcontrol_7.4.4-1_all.deb

Optionally, install the FAHViewer::

        sudo dpkg -i --force-depends fahviewer_7.4.4_amd64.deb

Done. The FAHClient is installed and running as a service. Manage, monitor and update settings using the FAHControl.

Terminal installation for RedHat / CentOS / Fedora
----------------------------------------------------

Download the installation package files; 64-bit versions shown. If using an i386/i686 32-bit OS version, download those files as appropriate from the client Download page::

        wget https://download.foldingathome.org/releases/public/release/fahclient/centos-5.3-64bit/v7.4/fahclient-7.4.4-1.x86_64.rpm
        wget https://download.foldingathome.org/releases/public/release/fahcontrol/centos-5.3-64bit/v7.4/fahcontrol-7.4.4-1.noarch.rpm
        wget https://download.foldingathome.org/releases/public/release/fahviewer/centos-5.3-64bit/v7.4/fahviewer-7.4.4-1.x86_64.rpm

Install the FAHClient::

        sudo rpm -i --nodeps fahclient-7.4.4-1.x86_64.rpm

Note: Fedora / RedHat .rpm packages do not support prompting for setup information. Instead, the client is set to pause on start so initial setup information may be entered through the FAHControl interface.

Install the FAHControl application.  Root privileges are required::

        sudo rpm -i --nodeps fahcontrol-7.4.4-1.noarch.rpm

Optionally, install the FAHViewer::

        sudo rpm -i --nodeps fahviewer-7.4.4-1.x86_64.rpm

Done. The FAHClient is installed and is ready to run as a service. Open FAHControl, enter user information, then unpause the client. Manage, monitor and update settings as needed.

Note: If the FAHControl application still has dependency issues with the installed version of Python, there is a workaround to copy the FAH Python files to the newer Python folder.  These commands assume that FAH is set to use Python 2.6, and Linux has Python 2.7 installed.

Create a link from the newer version to the older version::

        cd /usr/lib

        sudo ln -s /usr/lib/python2.7 /usr/lib/python2.6

Copy the fah module from the old location to the new location::

        sudo cp -R /usr/lib/python2.6/site-packages/fah /usr/lib/python2.7/site-packages/fah

This resolves the FAHControl dependency and will allow the application to run in the newest distributions of Linux.

Note that using this virtual link to Python may cause Yum to complain the next time a Python update is available.  Removing FAHControl from the RPM database will resolve this problem::

        sudo rpm -e --justdb FAHControl
