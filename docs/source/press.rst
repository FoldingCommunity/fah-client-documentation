==========
Press Info
==========

.. contents:: Table of Contents
   :depth: 4

How Did This All Come Together?
===============================

----------------------------------------------------
Folding\@home’s efforts in computational drug design
----------------------------------------------------

Do you have any specific examples?
----------------------------------
We’ve used Folding\@home to produce a lot of results towards drug design, 
and we’ve listed many of the publications on our `Papers page <https://foldingathome.org/papers-results/>`_. 
Several scientists in my lab are interested in drug resistance. 
As an example, they’re trying to understand how bacteria can develop an immunity to vancomycin, an important antibiotic that’s often used as a last resort. 
Beta-lactamase is also an important drug target due its ability to break down antibiotics like penicillin, 
and we hope to be able to design drugs to disable its functionality.

We’ve received several grants to study the ribosome, a large and highly complex molecular machine that manufactures proteins. 
About half of all antibiotics work by preventing bacterial ribosomes from synthesized important proteins. 
One of the scientific questions revolving around ribosome is why is there a large tunnel inside it through which proteins exit after being synthesized. 
We would like to understand the inside surface of this tunnel, as it would be useful to understand how key antibiotics interact with the ribosome. 
Many scientists are still very uncertain about the function of many proteins attached to the ribosome, so we’ve been studying those as well. 
The ribosome is so large and complex that it’s really been pushing the boundaries of what we can do on Folding\@home.

We have some work published in the drug design arena (for example, see the FKBP work done by Shirts and Jayachandran), 
but much of what we’re most excited about has not been published yet. We are mainly interest in three areas of computational drug design: 
cytokine-cytokine receptor interaction inhibition, development of novel chaperone inhibitors, and novel antibiotics to target the ribosome.

How about your work in drug design?
-----------------------------------
As our work matures, we have been looking to take the next steps involved in computational drug design. 
Our work here focuses on building a complete pipeline, 
starting with new methods for docking (work by Kim Branson in the Pande lab) to filter a million molecule library down to 100 to 1000 molecules 
and then use free energy methods (work by Guha Jayachandran, Michael Shirts, and John Chodera in the Pande lab) to filter this down to 10 to 100 molecules 
to assay experimentally (currently done by Kim Branson in the Pande lab and in collaboration with other labs as well).

How is FAH being used to implement computer-aided drug design?
--------------------------------------------------------------
One of the crucial steps in drug design is understanding how two molecules bind to each other. 
The two critical issues in a computational approach is speed and accuracy. 
Usually one has to trade one for the other and use a computationally efficient method like docking, at the cost of some accuracy, 
or use a computationally demanding method like free energy calculations, but at the cost of low throughput. 
With distributed computing and a set of complementary methods (both docking and free energy calculations), 
we can have it both ways — with the goals of high throughput and high accuracy. Distributed computing is a key aspect to this, 
as it allows us to do calculations otherwise impossible.

Most rational drug design efforts assume the target protein exists in a single structure and that the active site of the protein allows the protein to perform its function. 
With this in mind, the only way to manipulate a protein’s activity is with inhibitors that bind the active site tightly enough to block it from performing its intended function. 
Unfortunately, this strategy only works for ~15% of proteins, greatly limiting the number of proteins we can manipulate for therapeutic purposes. [1]_ 
My colleague, Dr. Gregory Bowman, has used Folding\@home to show that proteins are actually flexible, 
and he has used a process called allostery to indirect manipulate the active site, ultimately affecting the protein’s activity. [2]_

The Folding\@home project has been running for over ten years. How did it begin?
--------------------------------------------------------------------------------
In 1999, I started my position a professor at Stanford University, heading a research group. 
In order to push the envelope on what could be accomplished by my research group, 
it became clear that we would need to make a major push in computational power to perform our research of interest.

One of the first challenges was to develop a way to efficiently use distributed computing for our research. 
Not all problems are well-suited to distributed computing and ours was on the surface — not particularly well suited. 
However, after the development of novel algorithms, 
we discovered a statistical technique which allowed for distributed computing to make significant advances in what we do.

What is distributed computing?
------------------------------
Even back then, the calculations we wanted to do would take about a million days on a fast processor. 
So it seemed natural that we might be able to get it done in 10 days if we had access to 100,000 processors. 
By using distributed computing, we can split up the simulation, run each piece through a computer, and then combine them together afterwards. 
This really sped up our results.

Why don’t you just use a supercomputer?
---------------------------------------
It’s still very difficult to get an atomic-level simulation to run on a supercomputer. 
These systems are extremely expensive to build and operate, and you never get the supercomputer to use for yourself; 
you have to share the processors with other researchers. 
The few supercomputers that do perform molecular simulations have been specifically designed for the purpose, 
and all of them are several orders of magnitude slower than Folding\@home.

------------------
Science background
------------------

How can you prevent this from happening?
----------------------------------------
Once we understand how a protein folds, we can start designing drugs to prevent it from misfolding. 
Computer simulations will be extremely helpful here, allowing us to greatly reduce the time and costs involved in therapeutic drug design. 
There’s also an exciting connection between biology and nanotechnology, and for decades it has been a dream to be able to rationally design drugs. 
We want to be able to create drugs like we create bridges. What I mean is you design a bridge and cars go over it and it works. 
Using this analogy for designing drugs, we first create a bridge, 
send some rats over it and if it they survive, we try humans who really want to cross the bridge. It is still very much empirical. 
The dream is to design molecules the way we design macroscopic objects. 
Sounds easy, but with everything so small you must be really, really accurate and that is very computationally demanding.

What are proteins and why do they need to fold?
-----------------------------------------------
They are nature’s nanomachines. Proteins are the molecules in the body that it uses to get everything done. 
They act as catalysts to speed up chemical bonds that might take a billion years through other types of biological machinery. 
So whenever something needs to get done in biology, odds are, proteins are at work. 
They all have different functions, some are like scissors, some bring bonds together. 
They participate in virtually ever process within your body. 
If you think about the use of building nanomachines today, biology solved this millions of years ago. 
It amazes how well this works in the body.

Proteins are essentially sequences of amino acids, and they start off resembling a long stretched-out ribbon. 
Before they can do any work, they need to fold up into a functional three-dimensional shape. 
This shape largely determines what the protein can do in the body. 
Remarkably, proteins often spontaneously fold themselves! However, this process of protein folding, 
while critical and fundamental to virtually all of biology, remains a mystery.

What happens when the process does not work?
--------------------------------------------
When proteins do not fold correctly, that is when trouble occurs. Misfolding could produce a protein in completely the wrong shape. 
Lots of ways this can occur. A human can be missing the protein, like in cystic fibrosis. 
What is more prevalent is there are a whole class of diseases that were thought not to be related to one another, 
such as Mad Cow, Alzheimer’s, Parkinson’s, types of cancer and ALS, that are actually related to protein misfolding. 
And the misassembly not only makes the molecules toxic and dangerous, 
but the misfolded proteins can cause other proteins to misfold and also become toxic.

-----------------
What does FAH do?
-----------------

Are there any cost to the donors?
---------------------------------
We don’t charge for our software or anything like that. 
Donors have already bought their computers, etc, but we don’t charge them anything — they are donating a great resource to us, 
so there’s no reason to ask them for more.

On the same note, we don’t sell any of Folding\@home’s results either.

Are there any major disadvantages to conducting the research in this way?
-------------------------------------------------------------------------
There are always pros and cons of different styles of research. 
If someone donated several billion dollars to Stanford for computing resources, we would be able to build a resource comparable to Folding\@home. 
However, that’s not possible. So, within a more realistic budget, 
distributed computing is the most cost efficient means to build a supercomputer of this enormous scale.

How accurate are Folding\@home’s predictions?
---------------------------------------------
The vast amount of information we obtain from Folding\@home on the nature of folding and misfolding 
(e.g. pathways, rates, free energy, etc) continues to demonstrate a quantitative validation to laboratory results. 
We are constantly testing Folding\@home’s results for their accuracy, as this is a critical aspect of our work –– to make predictions relevant for experiment.

We have a tight coupling between simulations and experiments. 
New simulations lead to new experiments which lead to new simulations. 
With this iterative process, we hope to first gain a better understanding of folding and misfolding, 
and then apply this understanding to the development of novel drugs and other types of therapeutics.

In the interests of getting people interested in the project, is it possible to explain what you do in layman’s terms?
----------------------------------------------------------------------------------------------------------------------
Our work centers around proteins. 
Thus, it is natural to ask “what are proteins and why do they ‘fold’?” Proteins are biology’s workhorses — its “nanomachines.” 
Before proteins can carry out their biochemical function, they remarkably assemble themselves, or “fold.” 
The process of protein folding, while critical and fundamental to virtually all of biology, remains a mystery. 
Moreover, perhaps not surprisingly, when proteins do not fold correctly (i.e. “misfold”), there can be serious effects, 
including many well known diseases, such as Alzheimer’s, Mad Cow (BSE), CJD, ALS, and Parkinson’s disease.

What benefits can these simulations of protein folding bring?
-------------------------------------------------------------
With simulations, one can study aspects of folding and misfolding (and related disease) that one could never see with just experiment alone. 
Simulations won’t replace experiment, but can be a critically useful tool to go beyond what one could solely do in the lab. 
Yet experiments will always be crucial for verifying a simulation. 
We are combining our simulation predictions with laboratory tests (either done in my lab or in collaborators). 
Working together, we can greatly push the boundary of what used to be considered to be impossible, even just a year or two ago.

With that said, what does Folding\@home do?
-------------------------------------------
Folding\@home is a distributed computing project which studies protein folding, misfolding, aggregation, and related diseases. 
We use novel computational methods and large scale distributed computing to simulate timescales thousands to millions of times longer than previously achieved. 
This has allowed us to accurately simulate folding for the first time, and to now direct our approach to examine folding related disease.

--------------------------
What have you done so far?
--------------------------

Could you summarize some of the key papers which have resulted from FAH?
------------------------------------------------------------------------
This is always tough to do (as it’s like asking someone with a bunch of kids which ones are his favorites), but here’s a sampling. 
See our `Papers page <https://foldingathome.org/papers-results/>`_ for more details and the paper #’s I’m refering to. 
Google has a list of our most cited papers: 
http://scholar.google.com/citations?user=cWe_xpUAAAAJ

de novo simulations of protein folding with quantitative agreement with experiment

| While paper #1 (Shirts and Pande, Science, 2000) got the ball rolling, 
  paper #8 (Snow et al, Nature, 2002) was important since it was the first time that experiment 
  and simulation could really match in this sort of quantitative fashion. 
  It was a test of many aspects of FAH and turned out quite well quantitatively.
| Paper #17 is another good example of this, where we compared to multiple experimental methods.
| This early work has been followed up by numerous works after to better understand folding, 
  including folding in vitro (53, 49, 45, 42, 37, 35, 33, 24, 23, 22, 19, etc) and models of in vivo (#50, #36).

| **New drug design methodology**
| We have also been pushing the boundaries of what can do with computational drug design 
  (method in paper #29, results in paper #31 and #43, where we showed that our methods were very accurate, for a target of pharmaceutical relevance)

| **New methodology to simulate folding on distributed networks**
| We have also had major efforts to further enhance our methods to push FAH to do more and more. This includes papers 54, 49, 46, 40, 32, 27, 26, 19, etc.

| **Applications to disease**
| Most of the exciting work is still under peer review 
  (I think it always feels like that for scientists, as it takes ~1 year for review/publication), 
  however some highlights that are already out include our work on cancer (papers #39 and #20) and lipid fusion, 
  relevant for viral infection (papers #41, #47, #51)

What advances have you made in your research since the Folding\@home project began?
-----------------------------------------------------------------------------------
We’ve been able to push the boundary for simulations by several orders of magnitude and used it to make advances in understanding protein folding, 
misfolding, and related disease. Check out our Awards page for what others have said about us.

What are your goals with Folding\@home?
---------------------------------------
In the early years of Folding\@home we concentrated on developing new methods to tackle the computational challenges of simulating protein folding 
and applying these methods to gain new insights. 
In the last 5-7 years, we have been working on using these methods and insights to simulate Aß protein misfolding, 
a key process in the toxicity of Alzheimer’s Disease (AD). 
Our current goal is to use FAH for the development of new therapeutic strategies for AD. 
I feel that we are very much on track and we have seen some interesting results towards that goal.

.. [1] `Hopkins, 2002 <http://www.ncbi.nlm.nih.gov/pubmed/12209152>`_
.. [2] `Bowman, 2012 <http://www.pnas.org/content/109/29/11681>`_