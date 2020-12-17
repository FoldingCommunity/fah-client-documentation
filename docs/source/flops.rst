=====
FLOPS
=====

.. contents:: Table of Contents
   :depth: 2

What is a FLOP?
===============
FLOP is an acronym for Floating Point OPeration. Often one refers to the FLOPS, meaning the Floating Point Operations Per Second. 
The FLOPS is a measure of a computer’s performance, especially in fields of scientific calculations that make heavy use of floating point calculations.

What is a TFLOP (or Teraflop)?
==============================
A Teraflop is a trillion flops (or 10^12 FLOPS). 
Most supercomputers are of a Teraflop scale, whereas the next generation are designed to be in the Petaflop (10^15 FLOPS) scale. 
Please note FAH already runs in the Petaflop scale.

What are native FLOPS?
======================
We refer to the FLOP count on a given hardware as the native FLOP count. 
For example, an exponential on a GPU is one native GPU FLOP but many native x86 FLOPS.

What are x86 FLOPS?
===================
x86 FLOPS are an estimate of how many FLOPS a given calculation would take on an x86 class CPU.

Why are the ATI x86 FLOP numbers half of the ATI native FLOP numbers?
=====================================================================
Due to a difference in the implementation (in part due to hardware differences), 
the ATI code must do two force calculations where the x86, Cell, and NVIDIA hardware need only do one. 
This increases the overall native FLOP count for ATI hardware, but since these are not useful FLOPS in a sense, 
we did not include them in the x86 count.

Why are the x86 FLOP counts generally higher?
=============================================
The GPUs are more efficient at certain mathematical functions (eg exponential, sine, and cosine) 
and thus native GPU FLOP counts underestimate their performance relative to x86 hardware. 
In our x86 FLOP count metric, we have attempted to even this out.

Why aren’t the differences between native GPU and x86 FLOP counts even greater?
===============================================================================
In the end, much of the code uses simpler operations (add, multiply, divide, etc) which counts as one FLOP under both systems. 
The instructions which are much more different (e.g. exp(x)) are more rare (say 1/10th the number of instructions) 
and thus the overall difference is closer to 2x.

What conversion did you use for GPU to x86 FLOPS?
=================================================
For native GPU FLOPS, we tried to count each operation as just one FLOP, so a sqrt is one FLOP and a reciprocal sqrt is two FLOPS, etc., 
which leads to native GPU FLOP counts of the form:

- ``Sqrt = 1``
- ``Rsqrt = 2``
- ``Log = 1``
- ``Exp = 1``
- ``Acos = 1``
- ``Cos = 1``
- ``Sin = 1``
- ``Dot3 = 5``
- ``Cross3 = 9``

For x86 FLOPS, we followed

http://ai.stanford.edu/~paskin/slam/javadoc/javaslam/util/Flops.html

Which, for example, leads to x86 FLOP counts:

- ``Sqrt = 15``
- ``Rsqrt = 16``
- ``Log = 20``
- ``Exp = 20``

Are FLOPS consistent between different types of architectures?
==============================================================
No, different hardware can compute the same quantities differently. 
Typically, an addition or a multiply operation is always considered to be one FLOP, 
but more complex functions such as exponential, sine, or cosine, are less clear.

Is there a way to account for these differences to allow for an “apples to apples” comparison
=============================================================================================
One of the most common ways to do this is to use the same FLOP count for a given instruction no matter how the native hardware performs. 
Due to its ubiquity, the x86 architecture is often used as the reference architecture for this purpose. 
This makes sense in Folding\@home as well due to the ubiquity of x86 hardware involved in the project.