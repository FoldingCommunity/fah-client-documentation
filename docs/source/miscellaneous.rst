=============
Miscellaneous
=============

.. contents:: Overview
   :depth: 2

What do the pictures of proteins show?
======================================
We use several representations for showing proteins, including all-atom, stick, and Richardson cartoon representations. 
The colors are used to highlight specific parts (but that may be specific atoms, atom types, or structural characteristics, 
depending on the context). To learn more, Wikipedia has some nice articles about this:

| http://en.wikipedia.org/wiki/Protein_structure
| http://en.wikipedia.org/wiki/Alpha_helix
| http://en.wikipedia.org/wiki/Beta_sheet

Where did the logo come from?
=============================
Our logo is an abstract representation of our goal: to go from the protein sequence encoded in the genome to the protein’s structure. 
The double helix on the left of the logo denotes the genome (DNA is a double helical molecule) 
and the arrows on the right are representations of protein structure (beta sheet structure is often drawn as ribbons with arrows).

Do you have web buttons that I can download to use with links to your site?
===========================================================================
How about this? (thanks to RPH IV)

.. image:: https://foldingathome.org/wp-content/uploads/2016/09/FAHlogoButton.jpg
   :alt: Folding@home distributed computing

How much power/money does keeping a FAH running 24/7 on a computer use?
=======================================================================
Roughly, a CPU uses about as much power (watts) as a typical light bulb. 
Although power supplies on most computers are rated at 400 watts, average usage is lower. 
On average, a Pentium-type computer uses about 100 watts (if the monitor is off). 
So, the daily difference between off and running FAH is about 24×100 = 2.4 kWh. At $0.15 per kWh ( from PG&E here in California), 
this works out to about $0.36 per day. In general, lighting and climate control use a much larger share of household power than computers do. 
So the best bet for cutting costs and conserving energy would be to turn off lights, 
turn off your computer monitors (which use more power than a CPU), and turn down the heat.

What about security issues?
===========================
We have worked very hard to maintain the best security possible with modern computer science methodology. 
Our software will upload and download data only from our data server here at Stanford. 
Also, we only interact with FAH files on your computer (we don’t read, write, or transmit any other files, 
as we don’t need to do so and doing so would violate our privacy policy). 
The Cores are also digitally signed (see below) to make sure that you’re getting the true Stanford cores and nothing else.

How is this possible? 
We take extensive measures to check all of the data entering your computer and the results we send back to Stanford with 2048 bit digital signatures. 
If the signatures don’t match (on either the input or the output) the client will throw away the data and start again. 
This ensures, using the best software security measures developed to date (digital signatures and PKI in version 3.0), 
that we are keeping the tightest possible security. 
Finally, the clients are available for download only from this web site (or in certain cases, also from our commercial partners 
such as Sony, NVIDIA, and ATI), so that we can guarantee the integrity of the software. 
We do not support Folding\@home software obtained elsewhere and prohibit others to distribute the software.

Why no client version for IRIX, Solaris, OS-2, AMIGA, Commodore, Macintosh OS9, iPhone, Smart Phone, ARM chip, XBox, Wii, etc.?
===============================================================================================================================
We’ve been deluged by requests for other versions. Due to limited resources, we can only support a few client versions. 
We try to pick operating systems and hardware types which are likely to be popular with donators, 
that we can suitably support in house, and that will perform well on the scientific calculations.

What are you going to add in later versions of the software?
============================================================
A good place to hear about new versions, beta versions, etc., is Vijay’s blog, i.e. the Project News page, and the Folding Support Forum.