=====================
Running Folding\@Home
=====================

.. contents:: Table of Contents
   :depth: 2

Are there any limits to how long my machine can take to finish a work unit (WU)?
================================================================================
Yes. Work Units are serial in nature. When a completed WU is sent back, a new work unit is generated from those results. 
This must happen many times over within each project (group of work units). 
A generation 1 work unit must be turned in before a generation 2 work unit is created and sent out.

To keep these generations moving along, 
we have to set expiration deadlines in the event a work unit is not uploaded in a timely manner (lost, deleted, whatever). 
These unfinished work units “expire” and are reassigned to new machines. 
You will still receive credit for all WUs completed and uploaded prior to the Timeout (formerly preferred deadline). 
However, after the Timeout, 
your contribution is not as useful scientifically because another copy of that work unit had to be sent out to another contributor. 
Even if you eventually complete the work unit, that other contributor still had to process duplicate work to assure the science moves forward. 
And it would be unfair not to also credit that second contributor.

Even so, full credit is given up until the Deadline (formerly Final Deadline). 
After the Deadline has expired, the client will automatically discard the work unit and download new work. 
If you have trouble completing work units before the Timeout (formerly Preferred Deadline), 
it is recommended to either run the FAH client more hours each day, or to run the client on a faster computer.

As we move to larger and longer WUs, we will extend the expiration time as needed. 
Deadlines vary on the order of a few days to a several weeks, depending on the nature of the WU. 
Turn in a work unit just before the deadline is not the goal. 
It is most helpful to the project to return work units as quickly as possible. 
And how these deadlines are determined is explained a few answers below.

Can I download more than one unit at a time?
============================================
The algorithm we use works best if everybody downloads one work unit at a time, and checks back after each unit is completed. 
Therefore no option to download multiple units is available.

However, it is possible to work on multiple WUs at once; 
our latest client may do this by assigning each WU to different processing components in your computer. 
Folding\@home differs from many other projects in that it is important for WUs to be completed in a timely manner. 
It is far better to get a single WU done at full speed than to complete two WUs at half speed.

Does Folding\@home run on my graphics chip or GPU?
==================================================
Yes it can. Our client will automatically set this up by default. 
Folding\@home was the very first distributed computing project to utilize these specialized chips for distributed computing or for molecular dynamics simulations. 
For certain types of calculations, we’ve seen GPUs give us a 20-30x speedup over their CPU-based counterparts. See the GPU and High Performance FAQs. 
We’ve heard a few reports that folding on GPUs can impact system performance, and we are currently working towards measures to resolve the issue.

How can I configure the client using flags?
===========================================
Please see the Configuration FAQ.

How can I make sure my results are being sent back and used? How can I tell how much work I’ve processed?
=========================================================================================================
To find out data that has been reported back you can check the Stats page for Individual stats, Team stats, and overall Project stats. 
This usually updates at the top of the hour. 
If your computer is returning data, you should see your username there along with the number of work units completed. 
If your name isn’t there, 
then either it hasn’t finished a unit yet (this can take a few days, or even longer with an older computer) or the list hasn’t been updated yet. 
Check back in an hour or two, and it should be there . . . as long as you remember correctly what you typed in for your donor user name. 🙂

How do I manually adjust the priority of the Folding\@home core?
================================================================
The work is done by the fahcore, not the client process, so changing the priority on the client has no impact on performance. 
The priority for the fahcore is set to “Idle” by default (but displays as normal in Task Manager). 
The client is already designed to use all spare CPU cycles, so changing the Windows priority is unnecessary. 
If the FAH client is competing with another process running at “Idle” such as a background AV scan, there is a client option to run at a “Low” priority.

How do the results get back to you?
===================================
Your computer will automatically upload the results to our server each time it finishes a work unit, and download a new work at that time.

How long does it take to finish a work unit? How do you measure a work unit?
============================================================================
This varies, of course, on the speed of the computer and the size of the protein under study. 
Depending on the protein and the properties studied, different size work units may be used. 
The `Project Summary page <https://apps.foldingathome.org/psummary.html>`_ has information on particular proteins’ sizes and the deadlines allotted for completion.

I just finished a WU and now I got another for the same protein. Is there something wrong?
==========================================================================================
No, everything is fine. Each Work Unit is identified using four numbers, in the format: Project(Run, Clone, Generation). 
Each WU gives us additional information about the dynamics of that protein, so it is important to us. 
We often need thousands of WUs per protein to fully understand its folding process. 
Unlike some other distributed computing projects, (SETI\@home for example) our Work Units are processed to completion only once. 
It would therefore be extremely unusual to be reassigned the exact same WU.

What if I turn off my computer? Does the client save its work (i.e. checkpoint)?
================================================================================
Periodically, the core writes data to your hard disk so that if you stop the client, 
it can resume processing that WU from some point other than the very beginning. 
With the Tinker core, this happens at the end of every frame. With the Gromacs core, 
these checkpoints can happen almost anywhere and they are not tied to the data recorded in the results. 
Initially, this was set to every 1% of a WU (like 100 frames in Tinker) and then a timed checkpoint was added every 15 minutes, 
so that on a slow machine, you never lose more that 15 minutes work.

As proteins become more complex and run longer, 
it is better to have more frames in a WU so that you don’t lose so much progress if you have to restart – - 
hence WUs that have 400 frames instead of 100. That still doesn’t take the speed of the machine into account. 
A fast machine completes a frame in a few minutes while a slow one may take hours, 
and the donor with the slow machine still doesn’t want to lose 99% of those “hours” 
yet the fast machine doesn’t really want the overhead of writing the checkpoints every “few minutes” – - 
and neither of them wants the upload time associated with results containing many frames.

Starting in the 4.x version of the client, you can set the 15 minute default to another value (3-30 minutes).

Thanks to Bruce Borden for this FAQ entry.

What is simulation instability?
===============================
The simulation of molecular motion involves a great deal of computation. Each run consists of a number of time steps (each very small). 
At each time step, the position of the various atoms is calculated and updated, based on a number of factors. 
Sometimes, the simulation enters into a state that is not legal (i.e. atoms are too close, bonds are in impossible angles, etc.). 
At times like this, the Core exits, and information is uploaded to the server. The client will then get another assignment. 
If your computer is stable, then you haven’t done anything wrong. 
On unstable computers, it is possible that the simulation instability was brought on by a fault of the system rather than something intrinsic to the work unit. 
Because of this, a work unit may be sent out again at some time if it is returned as having run into instability. 
In a given project, we expect a small percentage of units to encounter legitimate instability.

Why should I update my Folding\@home software to the current version?
=====================================================================
We are continuously improving the Folding\@home software and adding new features. 
We release new versions to fix bugs reported by the users to help make the project run as smoothly as possible.