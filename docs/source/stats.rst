==========================
Stats, Teams and Usernames
==========================

.. contents:: Table of Contents
   :local:

How do I choose a username?
===========================
To check if a name is already being used, use the search tool at our page here:

https://foldingathome.org/support/faq/stats-teams-usernames/

Type your name (where it says “YourName”) to see if that user name is already being used. 
You can also choose not to have a username and just donate your CPU time anonymously (user name = anonymous).

You may choose any name you like, as long as it contains only letters or numbers (to insert a space, you may use the underscore “_” character). 
If you choose your email address as your username, we will use the full email address but NOT print the full email address. 
Instead, just the part before the @ sign will be used in any stats listing, etc. User names are also case sensitive.

------------------------------------------------------
Are there any characters I should avoid in a username?
------------------------------------------------------
Yes. We strongly recommend sticking to just letters, numbers and underscore. 
Right now, we reserve the characters # ^ ~ \|. # is used for firewall differentiation (see above). 
We want to save ^ \| and ~ for other problems which might come up. 
Also, don’t put spaces in your username; please use some character like “_” instead. 
Finally, please note that usernames are case sensitive, so “Dave” and “dave” and “dAVE” are all different usernames.

How do I start a Team or how do I join a Team?
==============================================
There are many teams already folding for the project. One of those teams may have lead you here. 
To join that team, simply enter their team # in to the client setup when you install the client. 
Or you can start a new team using the Create a Team page linked from the `Stats <https://foldingathome.org/statistics/>`_ page.

How can I change my username (donor name)?
==========================================
The simplest way to change your username is to go to the Configure window (click the Configure button on the upper left corner of the screen). 
You can change your username at any time. However, old work units will remain credited to the old username.

I’m running multiple machines behind a firewall. Can they all have the same username?
=====================================================================================
Yes. They can all have the same name.

How can I get a copy of all of the current stats?
=================================================
| Please feel free to download 
| https://apps.foldingathome.org/daily_user_summary.txt or 
| https://apps.foldingathome.org/daily_team_summary.txt 
| These files are updated every 3 hours. Please DO NOT run a crawler on our cgi pages. Such actions will result in your IP being permanently banned.

How do you decide how much credit a work unit is worth? How do you determine how many points a work unit is worth?
==================================================================================================================
We have a single benchmark machine, its most important component is its processor: a Intel(R) Core(TM) i5 CPU 750 @ 2.67GHz. 
The machine’s OS is Linux. Here are the steps that we use to determine points for a project:

1. Take a WU from a project and run it on the benchmark machine until it finishes.
2. Measure the time it took to complete. Base credit awarded for the WU is then just a scaling factor multiplied by this time.
3. The timeout and deadline values are also simple functions of the time it took to complete. 
   These are set primarily to give a donor a reasonable amount of time to finish a WU, 
   but short enough so that any WU that gets sent out but not processed 
   (e.g. donor quits FAH, forgets to re-start that WU, their computer dies, etc) can be retrieved and sent out again in a reasonable amount of time. 
   Thus these values are set depending on what kind of hardware a project is being run on (uniprocessor, SMP, GPU) 
   and how long the WU took to finish on the benchmark machine.
4. The k-factor, a coefficient in awarding bonus points, is currently set to a baseline value of 0.75, 
   but may vary depending on the scientific value of a project.

**The Folding@home software on your computer calculates Total Points as follows:**

``final_points = base_points * max(1, sqrt( k * deadline_length / elapsed_time))``

Note that the max(1, …) ensures that final_points are never lower than base_points, deadline_length is the deadline aka final deadline, 
and elapsed _time is the length of time from when the WU was assigned, to when it was uploaded, including transit time. 
Deadline_length and Elapsed_time are measured in days to one decimal point.

PPD is calculated as follows:

| ``PPD = 14.4 * base_points * max(1, sqrt( 14.4 * k * Expiration / TPF)) / TPF``
| Note that TPF is in minutes, in decimal form, not time format.

Note that GPU projects are now being benchmarked on the same machine, but using that machine’s CPU. 
By using the same hardware, we want to preserve our goal of “equal pay for equal work”. 
Our GPU methods have advanced to the point such that, with GPU FAHCore 17, we can run any computation that we can do on the CPU on the GPU. 
Therefore we’ve unified the benchmarking scheme so that both GPU and CPU projects use the same “yardstick”, which is our i5 benchmark CPU.

Please note that the very concept of a reference machine will mean that some WU benchmarking will vary from the performance on your machine. 
Even between P4s, there are significant differences in architectures over the years. 
Moreover, variations between FAH WUs can also lead to differences in benchmarking points.

Our goal is consistency within a given definition of a reference machine setup (described above), 
but beyond that the natural variation from machine to machine and WU to WU will never allow any point system to perfectly reflect what you get on your machine. 
See also the Points FAQ

How do you set the deadlines for the work units?
================================================
Each work unit is benchmarked on a dedicated Intel(R) Core(TM) i5 CPU 750 @ 2.67GHz. 
For most work units (although there may be exceptions, described in the next paragraph), we apply this equation:

| ``timeout = 20 * (daysPerWU) + 2``
| ``deadline = max(30* (daysPerWU) + 2,10)``

where daysPerWU is the number of days it took to complete the unit. 
The “+2″ days is there to give an additional buffer for fast WUs (to allow for servers down, etc). 
If 30*daysPerWU is less than 10 days, we set the deadline to 10 days, as a minimum time for all projects. 
The timeout is the time at which the WU is resent to another client and the deadline is the last time that we will give stats credit for the WU.

Occasionally, deadlines may be set shorter or longer than the above calculation indicates, 
but the reason for having deadlines at all is that the sooner we get back work units, the sooner we can put the results to good use. 
Also, different projects have different requirements server-side and may require shorter or allow longer deadlines 
(e.g. “pfold” calculations can often be run without any deadlines, whereas MREMD calculations work best with very tight deadlines). 
The assignment server does take machine performance into account in making assignments, 
thereby allowing slower machines to receive more appropriate work units.