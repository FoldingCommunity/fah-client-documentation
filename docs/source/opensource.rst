""""""""""
OpenSource
""""""""""

FAH is built from several open source tools, namely Gromacs (http://www.gromacs.org), TINKER (http://dasher.wustl.edu), 
and AMBER (http://ambermd.org/) for MD packages and MPICH for MPI (http://www-unix.mcs.anl.gov/mpi/mpich/). 
If you’re interested in checking out these codes, you should feel free to download them and check them out. 
One can compile a SMP version of Gromacs by using the latest Gromacs with MPICH. This would reproduce the SMP clients we have on FAH.

DATA
----
We’ve partnered with the Simbios National Biomedical Computing Center to provide data for download. 
If you’re curious, check out our first data set project page

https://simtk.org/home/foldvillin

We’ll be releasing more data as time goes on. Our hope is that by making the raw data openly available, 
this will greatly supplement the published results.

FULL OPEN SOURCING OF THE CLIENT
--------------------------------
We have not outsourced the client for several reasons, relating to client reliability and other issues. 
However, we’ve come up with a compromise — we have been developing a plug in architecture to allow people to write open source code 
that we can plug into our client. Visit the Folding Support Forum to discuss, ask questions, and show off your work.

ISN’T GROMACS A GPL’D CODE? WHERE’S THE SOURCE FOR YOUR MODS?
-------------------------------------------------------------
Folding@home has been granted a non-commercial, non-GPL license for Gromacs, so we are not required to release our source. 
We have analogous license for the other core codes. 
The copyright owners of any GPL code (in this case the owners are the Gromacs development team) can distribute the same piece of software with difference licenses in parallel. 
See the GPL FAQ for more info on this. However, we will release our patches back to the Gromacs tree (and have discussed this extensively with the Gromacs team).

We are also working to release our GPU code and other aspects of FAH mods in a new open library called OpenMM. 
You can learn more about that here: https://simtk.org/home/openmm.

It is important to note that we do release the scientific modifications back to the open source community, 
but do not release information which would enable donors to cheat on points, 
which some donors have done ruining the experience for many others.