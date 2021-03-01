======================================
Helpful Commands, Processes, and Notes
======================================

.. contents::
   :local:

Managing the Service
--------------------


Starting the service::
	systemctl start FAHClient

Stopping the service::
	systemctl stop FAHClient

Restarting the service::
	systemctl restart FAHClient






Note: There is no install guide or support in the forum for this type of expert only installation. The only support for command-line only installs is this:

Documentation::
        
        ./FAHClient --help

Configuration using config.xml::

        ./FAHClient --configure

Configuration with no config file (minimum flags)::
        
        ./FAHClient --user=Anonymous --team=0 --passkey=1385yourpasskeyhere5924 --gpu=false --smp=true
