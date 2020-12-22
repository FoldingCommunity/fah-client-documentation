===============
Points Overview
===============

.. contents:: Table of Contents
   :depth: 3

How are points determined?
==========================
Points are determined by the performance of each contributor’s folding hardware (CPU, GPU, etc.) relative to a reference benchmark machine. 
Before sending out any Work Units for a new project, we benchmark one or or more Work Units from that project on a dedicated machine. 
We then use the results to determine the points for all of the WUs in that project. 
On top of these base credits, we may add bonus points, described below.

When will my points, username, or team # appear in the Folding Statistics?
==========================================================================
When you first start, your username will not appear in the statistics until the software has completed its first Work Unit (WU). 
The stats are updated once an hour, on the hour, so they will not show up on the stats pages immediately. 
If you created a new team, it will appear right away.

Why are there deviations in the amount of points received?
==========================================================
Not all Work Units are the same. 
Some of the researchers in our group are studying the behaviors of small proteins, while others are focusing on larger and more complex systems. 
These differences cause deviations of points to be above or below the average. 
Some computer systems are more efficient at processing certain types of projects than others, 
which adds additional complexity to the goal of making the points fair, even, and balanced. 
Evening out these deviations is one of the reasons why we use a benchmark machine. 
We do additional balancing in our beta and advanced stages of testing before we distribute the work to all of Folding\@home.

Bonus Points
============
The prompt completion of Work Units (WUs) is very important for the science we’re doing. 
In order to study the proteins we’re interested in, we need be able get the results back quickly. 
A faster turnaround also means that we can launch projects that are larger and more difficult than ever before. 
So in 2010 we introduced the Quick Return Bonus (QRB), which gives extra points to users who rapidly and reliably complete WUs. 
The QRB has been fairly successful in aligning points with scientific value, and we will continue to use it.

----------------------------------------
What are the qualifications for the QRB?
----------------------------------------
The bonus is applied for users who use a passkey, have successfully returned at least 10 bonus-eligible WUs, 
have successfully returned 80% or more of assigned WUs, and returned the unit before its Timeout (formerly Preferred Deadline). 
Bonus points do not apply to partial returns.

--------------------------
How is the QRB determined?
--------------------------
We have a single benchmark machine, its most important component is its processor: an Intel(R) Core(TM) i5 CPU 750 @ 2.67GHz. 
The machine’s OS is Linux. Here are the steps that we use to determine points for a project:

1. Take a WU from a project and run it on the benchmark machine until it finishes.
2. Measure the time it took to complete. Base credit awarded for the WU is then just a scaling factor multiplied by this time.
3. The timeout and deadline values are also simple functions of the time it took to complete. 
   These are set primarily to give a donor a reasonable amount of time to finish a WU, 
   but short enough so that any WU that gets sent out but not processed (e.g. donor quits FAH, 
   forgets to re-start that WU, their computer dies, etc) can be retrieved and sent out again in a reasonable amount of time. 
   Thus these values are set depending on what kind of hardware a project is being run on (uniprocessor, SMP, GPU) 
   and how long the WU took to finish on the benchmark machine.
4. The k-factor, a coefficient in awarding bonus points, is currently set to a baseline value of 0.75, 
   but may vary depending on the scientific value of a project.

The Folding\@home software on your computer calculates Total Points as follows:

``final_points = base_points * max(1, sqrt( k * deadline_length / elapsed_time))``

Note that the max(1, …) ensures that final_points are never lower than base_points, deadline_length is the deadline aka final deadline, 
and elapsed _time is the length of time from when the WU was assigned, to when it was uploaded, including transit time.  
Deadline_length and Elapsed_time are measured in days to one decimal point.

PPD is calculated as follows:

``PPD = 14.4 * base_points * max(1, sqrt( 14.4 * k * Expiration / TPF)) / TPF``

Note that TPF is in minutes, in decimal form, not time format.

Note that GPU projects are now being benchmarked on the same machine, but using that machine’s CPU. 
By using the same hardware, we want to preserve our goal of “equal pay for equal work”. 
Our GPU methods have advanced to the point such that, with GPU FAHCore 17, we can run any computation that we can do on the CPU on the GPU. 
Therefore we’ve unified the benchmarking scheme so that both GPU and CPU projects use the same “yardstick”, which is our i5 benchmark CPU.

---------------------------
What projects have the QRB?
---------------------------
Right now, it is mainly applied to Work Units for multi-core processors. However, they will soon be applied to WUs for GPUs. 
As our GPU methods have matured, our plan is to treat all WUs identically. 
We can now do the same calculations (including implicit and explicit solvation) on both CPUs and GPUs. 
In years past, these two pieces of hardware were treated differently. This is no longer the case. 
Our plan is to introduce the Quick Return Bonus to GPUs as we roll out our new GPU core, FAHCore 17.