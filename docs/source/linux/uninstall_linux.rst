=========
Uninstall
=========

.. contents::
   :local:

This section describes how to uninstall V7 FAH application.

Please let the current Work Unit finish and upload (using “Finish”). Exit the FAHControl application.

Open a terminal window. Enter the command appropriate for your version of Linux:

Ubuntu::
  
        sudo dpkg -P fahclient


Fedora::

        su -c 'yum remove fahclient'


Press Enter.

Enter password when prompted.

Press Enter.

Repeat for the fahcontrol and fahviewer packages if also installed.

Uninstall is complete.
