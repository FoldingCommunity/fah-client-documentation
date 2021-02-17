====================
Command Line Options
====================

.. contents::
   :local:


Managing the system service
---------------------------

There are two options for running the FAHClient in Linux:

#. Run as a system service. This is the recommended and default option. The FAHClient service is installed automatically via the installer package, and will start at boot. Then control and configure the FAHClient with FAHControl. Note that FAHControl will not start or stop the FAHClient process. This setup uses /etc/fahclient/config.xml and runs in /var/lib/fahclient/. Do not run FAHClient directly when the service is running.
#. Run from command line. Alternately, with the service disabled, it is possible to run the FAHClient manually from the command line in a directory of your choice. FAHClient will run in the current directory and use a config.xml from the same directory.


Both of these options can be headless if choosing not to use FAHControl. The FAHClient can be configured for remote access by editing /etc/fahclient/config.xml, but please be very careful in doing so. The FAHClient is started and stopped via the service script in /etc/init.d/FAHClient::

        sudo /etc/init.d/FAHClient start
        sudo /etc/init.d/FAHClient stop


Services are started and stopped by root but the client will automatically drop root privileges when run this way. It runs in the restricted fahclient account for added security. Starting and stopping the service is however, not at all necessary if when using FAHControl. Instead pause/unpause the FAHClient. When paused the FAHClient should idle in the background using negligible resources.
The plain command line only FAHClient tarball is available for download here.

Note: There is no install guide or support in the forum for this type of expert only installation. The only support for command-line only installs is this:

Documentation::
        
        ./FAHClient --help

Configuration using config.xml::

        ./FAHClient --configure

Configuration with no config file (minimum flags)::
        
        ./FAHClient --user=Anonymous --team=0 --passkey=1385yourpasskeyhere5924 --gpu=false --smp=true
