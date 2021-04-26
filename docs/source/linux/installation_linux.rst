Installation
============

.. contents::
   :local:


Overview
--------

This section describes the recommended method for installing the V7 FAH software for an individual client slot using a software package in Linux. A first time installation is assumed. And unless otherwised noted, the default setting for each option is the recommended setting.


Requirements
------------

This document requires root access to the system.


Installation for Debian, Mint, and Ubuntu
-----------------------------------------

Identify and Download the Latest F@H Version
********************************************

.. note::

   Please note that in order to satisfy fahcontrol dependencies, you may need to manually configure the python-gtk2 repository for your distribution. Additional information can be found here: https://packages.ubuntu.com/bionic/amd64/python-gtk2/download


#. Navigate to https://foldingathome.org/alternative-downloads/
#. Right click the deb links, and select 'Copy Link Location'
#. Download the latest identified F@H version to your local machine::

	su root
        cd [Downloads_Directory]
        wget https://download.foldingathome.org/releases/public/release/fahclient/debian-stable-64bit/[version]/fahclient_[version]_amd64.deb
        wget https://download.foldingathome.org/releases/public/release/fahcontrol/debian-stable-64bit/[version]/fahcontrol_[version]-1_all.deb
        wget https://download.foldingathome.org/releases/public/release/fahviewer/debian-stable-64bit/[version]/fahviewer_[version]_amd64.deb


Install the Packages
********************

1. Install the FAHClient. After the package installs, Folding@Home processes will begin running and consuming CPU cycles::

        apt install ./fahclient_[version]_amd64.deb

2. Install the FAHControl application. FAHControl will show “offline” or “connecting” status until the FAHClient is running, either started automatically (strongly recommended) or started manually::

        dpkg -i --force-depends fahcontrol_[version]-1_all.deb

3. Optionally, install the FAHViewer::

        apt install ./fahviewer_[version]_amd64.deb
 
4. Complete post install steps.




Installation for RedHat, CentOS, and Fedora
-------------------------------------------



Identify and Download the Latest F@H Version
********************************************

#. Navigate to https://foldingathome.org/alternative-downloads/
#. Right click the rpm links, and select 'Copy Link Location'
#. Download the latest identified F@H version to your local machine::

        wget https://download.foldingathome.org/releases/public/release/fahclient/centos-[version]-64bit/[version]/fahclient-[version]-1.x86_64.rpm
        wget https://download.foldingathome.org/releases/public/release/fahcontrol/centos-[version]-64bit/[version]/fahcontrol-[version]-1.noarch.rpm
        wget https://download.foldingathome.org/releases/public/release/fahviewer/centos-[version]-64bit/[version]/fahviewer-[version]-1.x86_64.rpm


Install the Packages
********************

#. Install the FAHClient. Note that Fedora / RedHat .rpm packages do not support prompting for setup information. Instead, the client is set to pause on start so initial setup information may be entered through the FAHControl interface::

        rpm -i --nodeps fahclient-[version]-1.x86_64.rpm


#. Install the FAHControl application. Please note that it is not required to install fahcontrol on a headless (non-GUI) system::

        rpm -i --nodeps fahcontrol-[version]-1.noarch.rpm

#. install the FAHViewer. Please note that it is not required to install fahcontrol on a headless (non-GUI) system::

        rpm -i --nodeps fahviewer-[version]-1.x86_64.rpm

#. Complete post install steps.


Post Install Steps
------------------

Configure config.xml File
*************************

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
	  <slot id='0' type='CPU'>
	    <cpus v='2'/>
	  </slot>



.. note::

   Please note that modifying the number of cores to leverage may not be seen immediately. The existing work unit will need to complete before the updated core usage will be seen.


Configure Systemd Service
*************************

#. Open a new file for F@H::

        vi /etc/systemd/system/fahclient.service

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
        Restart=always

        [Install]
        WantedBy=multi-user.target

#. Save the file
#. Start the service::

        systemctl start fahclient

#. Verify service status::

        systemctl status fahclient



Configure Remote Access (Optional)
**********************************

#. Update the /etc/fahclient/config.xml file with the following stanza, while substituting in the IP address you want to allow::

         <!-- Grant remote web access to the following IP -->
         <allow>192.168.1.1</allow>
         <web-allow>192.168.1.1</web-allow>

#. Navigate to the Web Control page to verify access: http://[IP_Address]:7396/
