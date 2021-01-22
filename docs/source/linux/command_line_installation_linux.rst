Command Line Installation
==========================

.. contents::
   :local:



Overview
---------

Here are the basic command-line instructions to install and run the V7 Folding@home software.

Open the Terminal / Console application. Depending on the Linux distribution (Ubuntu, Fedora, etc.), OS version, and desktop engine (KDE, GNOME, Unity, etc.) the Terminal / Console application may be found in a variety of locations. It is typically located under Accessories or System Tools.  This is not for Linux running in Terminal mode (no GUI).

Type each command exactly as it appears, or cut and paste directly from this guide.

Note: The installation commands shown include options to continue even when exact dependencies are not met. The V7 software is rather generic and works with most, if not all, version of the various libraries.


Requirements
------------

This document assumes root access to the system.


Installation for Debian, Mint, and Ubuntu
-------------------------------------------------

Identify and Download the Latest F@H Version
********************************************

#. Navigate to https://foldingathome.org/start-folding/
#. Right click the deb links, and select 'Copy Link Location'
#. Download the latest identified F@H version to your local machine::

        wget https://download.foldingathome.org/releases/public/release/fahclient/debian-stable-64bit/[version]/fahclient_[version]_amd64.deb
        wget https://download.foldingathome.org/releases/public/release/fahcontrol/debian-stable-64bit/[version]/fahcontrol_[version]-1_all.deb
        wget https://download.foldingathome.org/releases/public/release/fahviewer/debian-stable-64bit/[version]/fahviewer_[version]_amd64.deb


Install the Packages
********************

#. Install the FAHClient. The package will prompt for initial setup information, user name, etc. Enter information or change as needed, and click OK::

        dpkg -i --force-depends fahclient_[version]_amd64.deb


#. Install the FAHControl application. Root privileges are required. FAHControl will show “offline” or “connecting” status until the FAHClient is running, either started automatically (strongly recommended) or started manually::

        dpkg -i --force-depends fahcontrol_[version]-1_all.deb

#. Optionally, install the FAHViewer::

        dpkg -i --force-depends fahviewer_[version]_amd64.deb

Done. The FAHClient is installed and running as a service. Manage, monitor and update settings using the FAHControl.



Terminal installation for RedHat, CentOS, and Fedora
------------------------------------------------------



Identify and Download the Latest F@H Version
********************************************

#. Navigate to https://foldingathome.org/start-folding/
#. Right click the rpm links, and select 'Copy Link Location'
#. Download the latest identified F@H version to your local machine::

        wget https://download.foldingathome.org/releases/public/release/fahclient/centos-[version]-64bit/[version]/fahclient-[version]-1.x86_64.rpm
        wget https://download.foldingathome.org/releases/public/release/fahcontrol/centos-[version]-64bit/[version]/fahcontrol-[version]-1.noarch.rpm
        wget https://download.foldingathome.org/releases/public/release/fahviewer/centos-[version]-64bit/[version]/fahviewer-[version]-1.x86_64.rpm


Install the Packages
********************

#. Install the FAHClient. Note that Fedora / RedHat .rpm packages do not support prompting for setup information. Instead, the client is set to pause on start so initial setup information may be entered through the FAHControl interface::

        rpm -i --nodeps fahclient-7.4.4-1.x86_64.rpm


#. Install the FAHControl application. Root privileges are required::

        rpm -i --nodeps fahcontrol-7.4.4-1.noarch.rpm

#. Optionally, install the FAHViewer::

        rpm -i --nodeps fahviewer-7.4.4-1.x86_64.rpm

Done. The FAHClient is installed and is ready to run as a service. Open FAHControl, enter user information, then unpause the client. Manage, monitor and update settings as needed.


Configure config.xml
********************

#. Open the config.xml file::

        vi /etc/fahclient/config.xml

#. Enter the desired configuration. The below example displays identifying a user, team, and 2 CPU cores::

        <config>
          <!-- Folding Slot Configuration -->
          <gpu v='false'/>

          <!-- Slot Control -->
          <power v='light'/>

          <!-- User Information -->
          <passkey v='123456789abcdefg'/>
          <team v='123456'/>
          <user v='First_Last'/> 

          <!-- Folding Slots -->
          <slot id='1' type='CPU'/>
          <slot id='2' type='CPU'/>




Configure System Service
************************

#. Open a new file for F@H::

        vi /etc/systemd/system/FAHClient.service

#. Insert the following text into the file::

        [Unit]
        Description=Folding@home V7 Client

        [Service]
        Type=simple
        User=fahclient
        Group=fahclient
        WorkingDirectory=/var/lib/fahclient
        ExecStart=/usr/bin/FAHClient --config=/etc/fahclient/config.xml --chdir=/var/lib/fahclient/
        PrivateTmp=yes

        [Install]
        WantedBy=multi-user.target

#. Save the file
#. Start the service::

        systemctl start FAHClient.service

#. Verify service status::

        systemctl status FAHClient.service

Troubleshooting
---------------

If the FAHControl application still has dependency issues with the installed version of Python, there is a workaround to copy the FAH Python files to the newer Python folder.  These commands assume that FAH is set to use Python 2.6, and Linux has Python 2.7 installed. Create a link from the newer version to the older version::

        cd /usr/lib

        sudo ln -s /usr/lib/python2.7 /usr/lib/python2.6

Copy the fah module from the old location to the new location::

        sudo cp -R /usr/lib/python2.6/site-packages/fah /usr/lib/python2.7/site-packages/fah

This resolves the FAHControl dependency and will allow the application to run in the newest distributions of Linux.

Note that using this virtual link to Python may cause Yum to complain the next time a Python update is available. Removing FAHControl from the RPM database will resolve this problem::

        sudo rpm -e --justdb FAHControl
