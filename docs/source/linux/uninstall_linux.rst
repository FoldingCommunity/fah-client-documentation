=========
Uninstall
=========

.. contents::
   :local:

This section describes how to uninstall V7 FAH application.

Please let the current Work Unit finish and upload (using “Finish”). Exit the FAHControl application.


Ubuntu, Mint, and Debian
------------------------


#. Identify currently installed folding@home packages::

	apt list --installed | grep fah

#. Remove the packages::

	 apt remove [package_name]



Red Hat, CentOS, and Fedora
---------------------------

#. Identify currently installed folding@home packages::

	rpm -qa | grep -i fah

#. Remove the packages::

	yum remove [package_name]


Cleanup Files & Directories
---------------------------

#. Cleanup files and directories created during package installation::

	cd /etc
	rm -rf fahclient

	cd /var/lib
	rm -rf fahclient
