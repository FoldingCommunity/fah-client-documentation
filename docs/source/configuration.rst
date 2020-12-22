===================
Configuration Guide
===================

.. contents:: Table of Contents
   :depth: 3

General configurations
======================
V7 has the “Configure” and the “Preferences” buttons to provide many configuration options.

As always, the default client settings are the recommended settings. 
If any change results in a problem, please revert back to the original setting.

Introduction
============
The Folding\@home (FAH) client typically runs well using the default settings for most people. 
However, the client can be configured or customized in different ways. 
For example, one may choose the amount of computing resources donated to FAH, or change when to download the next work unit.

The v6 client was customized using command line switches (i.e. -flags). 
The latest FAH software (V7) has an improved graphical interface that offers a lot of configuration flexibility, but it also supports command line switches. 
Configuration changes, including switches, can have a significant impact on the FAH client, good or bad, 
so only make a change when absolutely sure of what the change will do. 
It is always better to read the FAQs and understand the settings than to crash the client with experimentation and corrupt work units which loses points.

V7 was designed to utilize multiple CPU cores with a multi-cored CPU slot (formerly SMP slot) and a GPU slot for each supported GPU. 
This configuration uses a lot more resources compared to using just a single CPU core. 
While CPU and GPU folding are much more scientifically productive compared to their single core CPU slot counterpart, 
they should not be run on machines which cannot tolerate heavy use. 
If FAH is using too much resources, please adjust the slot configurations to suit the computing needs. 
See the suggestions below. See also the Installation Guides for basic setup instructions. 
And help is always available on the Folding Support Forum.

Note: When participating in FAH, these “buttons and levers” at the client level can be used to adjust the contribution level. 
Many donors find that tuning the client and their machine configuration can sometimes optimize their contribution. 
Please use only the controls provided by the client and the operating system; do not modify the cores or FAH data in any way. 
Doing so is the equivalent of providing a tainted donation. 
When tainted donations are detected, awarded points may be zeroed, further donations blocked by the Servers, 
and/or additional actions taken to correct the situation. 
We greatly appreciate the contributions to Folding\@home; please do not devalue the collective works by undermining the scientific results.

Switches (flags, options) for V7.4.x and v6.32
==============================================
Listed below are some of the more common switches (flags) used for v6.xx and V7.x.x. The Installation Guides describe how to add these flags. 
The “Additional Parameters” setting in the v6 client makes it easier to add switches than by editing a shortcut to the client.

How to change options (such as flags)
=====================================
This section describes how to add or change a client or slot option, also known as a flag or a switch, such as forceasm or advmethods. 
This procedure assumes expert knowledge of the V7 Folding\@home software, and familiarity with the list of the v6 to V7 flag changes.

The recommended procedure for adding or changing a client or slot option is through the FAHControl interface. 
Options can be set globally (for all slots) or set locally (for each slot). 
For example, all slots can fold for one specific team number, or each slot can fold for a different team number. 
Local (per slot) settings are configured on the Slots tab. Global (all slot) options are configured on the Expert tab. 
And many options work as either a local setting, or a global setting. 
As example, the client-type option with a value of advanced can be set for one slot, or all slots. 
But please be careful not to set both, as the resulting behavior may be unwanted.

Note: Options can be added manually by editing the FAHClient configuration file. 
However, this is risky as incorrect settings or typing mistakes may cause the current work unit to abort, 
the client to crash, or future points to be credited to someone other than you.

------------------------------------
Customize All Slots (Global setting)
------------------------------------
Click the FAHClient icon in the system tray. Select Advanced Control (aka FAHControl) (see figure 1).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG18TrayIcon.png
   :alt: FAHControl
   :align: center

Figure 1

The FAHControl interface is displayed (see figure 2).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG19FAHControl-1-500x444.png
   :alt: FAHControl-Interface
   :align: center

Figure 2

Click the Configure button (on toolbar).

The Configure window and Identity tab are displayed by default (see figure 3).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG20IdentityTab-1-500x404.png
   :alt: Configure-Window
   :align: center

Figure 3

Select the Expert tab.

On the Expert Tab, the Extra client options and Extra core options sections are shown (see figure 4).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF04bFAHControl-500x273.png
   :alt: Expert-Tab
   :align: center

Figure 4

Depending on the option to be changed, click the Add button in either the Extra client options section, or the Extra core options section.

Note: V7 options are typically set in the Extra client options section, while older fahcore options are set in the Extra core options section.

The Edit Options window, or the Edit Core Option window is displayed (see figure 5).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF06aFAHControl.png
   :alt: Edit-Options-1
   :align: center

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF06bFAHControl.png
   :alt: Edit-Options-2
   :align: center

Extra client options <– Figure 5 –> Extra core options

For a Client Option, enter the Name of the option (flag or setting) to change. Enter the Value for that option. 
The example of Name: client-type with Value: advanced is shown (see figure 6 left).

For an Extra Core Option, which are older flags passed directly to the FAHCore, only that exact flag is entered. 
There is no option name to enter, only the flag value. The example -np 2 is shown (include the dash) (see figure 6 right). 
Not all Extra Core Options are supported by all FAHCore types, and unsupported flags will be ignored.

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF07FAHControl-1.png
   :alt: Advanced-Options-1
   :align: center

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF07bFAHControl.png
   :alt: Advanced-Options-2
   :align: center

Extra client options <– Figure 6 –> Extra core options

Repeat as needed to add additional client or core options. 
Or click OK and then Save to save the changes and return to the main FAHControl screen.

Note: Depending on the option changed, 
FAHClient (system tray) may need to be closed (quit) and opened again for the option setting change to take affect. 
Additionally, the setting change may not take affect until the next work unit.

----------------------------------
Customize One Slot (Local setting)
----------------------------------
Click the FAHClient icon in the system tray. Select Advanced Control (aka FAHControl) (see figure 7).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG18TrayIcon.png
   :alt: FAHControl-Local
   :align: center

Figure 7

The FAHControl interface is displayed (see figure 8).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG19FAHControl-1-500x444.png
   :alt: FAHControl-Interface-Local
   :align: center

Figure 8

Click the Configure button (on toolbar).

The Configure window and Identity tab are displayed by default (see figure 9).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WIG20IdentityTab-1-500x404.png
   :alt: Configure-Window-Local
   :align: center

Figure 9

Select the Slots tab.

The current Folding Slots are listed (see figure 10).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF04FAHControl-500x280.png
   :alt: Folding-Slots
   :align: center

Figure 10

Select a Folding Slot to modify, and click the Edit button.

The Configure Folding Slot screen is displayed (see figure 11).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF05FAHControl-500x606.png
   :alt: Configure-Folding-Slot
   :align: center

Figure 11

Click the Add button.

The Edit Options window is displayed (see figure 12).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF06aFAHControl.png
   :alt: Edit-Options
   :align: center

Figure 12

Enter the Name of the option (flag or setting) to change. Enter the Value for that option. 
The example of Name: client-type with Value: advanced is shown (see figure 13).

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/WCF07FAHControl.png
   :alt: Advanced-Options
   :align: center

Figure 13

Click OK.

Repeat as needed to add additional slot options, or click OK and then Save to save the changes and return to the main FAHControl screen.

Note: Depending on the option changed, FAHClient (system tray) may need to be closed (quit) and opened again for the option setting change to take affect. 
Additionally, the setting change may not take affect until the next work unit.

----------------
Advanced Methods
----------------
|   ``v6: -advmethods``
|   ``V7: client-type     advanced``

Sets a client preference to request late stage beta work units if available. 
This is only a request for a specific type of work unit, and is never a guarantee the client will received this type of work unit. 
If none of these work units are available, and regular work unit will be downloaded instead.

This switch is not intended for machines where stability or usability are the primary concern (e.g. corporate or education environments). 
Its use may lead to the client running experimental projects, which may be less stable or much more complex. 
This setting is not recommended for a machine which is not constantly monitored. This setting may require more donor intervention. 
The availability of this class of WUs is based on the current projects that are running, so there is no guarantee the client will get these WUs. 
This setting has no affect on PPD.  PPD for these WUs are benchmarked and set exactly the same as every other work unit. 
However, due to an occasional instability, the WU might fail, which results in lost points, so overall PPD might decrease.

When beginning new simulation projects, 
they are carefully rolled out using a Quality Assurance (QA) protocol which involves internal testing by members of Pande Group, 
then testing by the Beta Team, release under Advanced Methods, before a final full deployment across all of Folding\@home. 
This gradual rollout is to prevent problematic WUs and software from getting released to the public 
and to allow donors to have some choice in terms of bleeding edge donations. 
The Advanced Method option tells the client to request WUs from projects which have past most — but not all — of their stability testing. 
Please use this option carefully, and report any problems you encounter to the appropriate section of the Folding Support Forum.

------------
Big Advanced
------------
|   ``v6: -bigadv``
|   ``V7: client-type     bigadv``

Sets a client preference to request extra large work units for multi-CPU socket class server systems. 
A minimum of 16 CPU cores is required for Assignment Server access, and to meet the extremely short deadlines. 
This is only a request for a specific type of work unit, and is never a guarantee the client will received this type of work unit. 
If none of these work units are available, and regular work unit will be downloaded instead.

In 2009, Dr. Kasson introduced a an experimental WU category called “bigadv”, intended for some of the most powerful computers participating in FAH. 
The initial core count requirement was 8 cores. 
Currently, bigadv WUs require a minimum of 16 CPU cores and have very tight completion deadlines, 
although that minimum requirement has been known to change over time. 
These WUs have a high scientific priority, and are so computationally demanding they could not run anywhere else on Folding\@home. 
They also consume much more RAM and Internet bandwidth, 
but in return a 20% increase in point value was added on top of the existing Quick Return Bonus points system.

Note: BigAdv work units are only available to Linux operating systems at this time. 
However, Windows availability may return in the future.

- July 2009 – Experimental BA program introduction, with 8 core minimum
- July 2011 – BA points curve adjusted downward, 50% to 20% target
- January 2011 – Core minimum raised to 16, deadlines shortened.
- May 2014 – Core minimum raised to 24, deadlines shortened.
- January 2015 – BA Experiment scheduled to end.

--------------
Big Work Units
--------------
This setting is typically used by the v6 client, and may be helpful to computers that are several years old. 
Big Work Units are typically larger in size in regard to upload size and RAM requirements. 
The Control Panel of the GUI-based v6 client offered an checkbox for these larger WUs. 
The command-line console v6 clients has “small”, “normal”, and “big” options which equate to expected file upload sizes of <5MB, 5-10MB, >5MB, respectively. 
This setting is not recommend for clients with dial-up modems, 
due to the large file sizes involved (and greater potential for transmission problems and WU loss). 
The availability of this class of WUs is based on the current projects that are running, so there is no guarantee the client will get these WUs.

All SMP WUs are hard coded to be considered Big WUs by the FAH client.

--------------------
Next Unit Percentage
--------------------
|   ``v6: not applicable``
|   ``V7: next-unit-percentage     XX``

Sets the work unit percentage completed as to when the V7 client downloads the next Work Unit (WU) while the current WU is processing, 
where XX is between 90-100%.  99% is the default setting.

v6 and previous clients would finish a Work Unit (WU), upload it to the Work Server, then download a new WU, and begin processing. 
One of the best new features in the V7 client is the ability to concurrently download a new WU just before the current one completes, 
or while the current one uploads.

Very fast computers, 
or computers on a very fast internet connection will find that changing this setting to 100% is the best balance between points and performance. 
Remember the bonus clock starts ticking when the WU is downloaded, so if downloaded earlier than necessary to keep the computer folding, 
the bonus points clock starts ticking down.

--------------
Pause On Start
--------------
|   ``v6: (the “prompt for connection” configuration setting is similar)``
|   ``V7: pause-on-start     true/false``

Sets the V7 client to not begin processing work units when started.

By default, V7 will start automatically at system startup. Adding this setting will put client in to a paused state. 
The client must be started with the “Fold” button to resume processing or download new work.