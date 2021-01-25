=========
Uninstall
=========

.. contents::
   :local:

This section describes how to uninstall V7 FAH application.

Please let the current Work Unit finish and upload (using “Finish”). Exit the FAHControl application.


Debian / Mint / Ubuntu
----------------------
  
        sudo dpkg -P fahclient



Fedora / CentOS / Red Hat
-------------------------

#. Identify currently installed folding@home packages:
	rpm -qa | grep -i fah
#. Remove the packages
	yum remove [package_name]	

