============
Requirements
============

.. contents::
   :local:

The new V7 software has the same basic hardware and operating system requirements as the previous clients. However, a few software specific requirements have changed to support newer features. Listed by slot type:

CPU Slot Requirements 
----------------------
- Recent 32 bit or 64 bit Linux distribution, Ubuntu 11.04, Red Hat 6.x, OpenSUSE 11.x
- Intel P4 1.4 GHz processor or newer, or AMD equivalent (modern multi-core processors recommended)
- Broadband internet connection or faster

CPU Notes
---------

- A limited selection of Projects are available for 32-bit
- A limited selection of Projects are available for single core processors, as the End Of Life for single core projects was announced in August 2013
- Projects for higher numbers of cores may require 64-bit and have shorter deadlines, generally requiring a client running at or close to 24/7


GPU Slot Requirements
---------------------

- Recent 64 bit Linux distribution, Ubuntu 11.04, Red Hat 6.x, OpenSUSE 11.x
- FAHClient running more than part time to meet shorter deadlines
- Broadband internet connection or faster
- 1 or more supported GPU video cards, see below 



AMD GPU Requirements
********************
- GPU3 – OpenCL – FAHCore_17
        - OpenCL compatible GPU, 5xxx series or newer, see full list
        - 14.4 AMD device driver or newer  
- GPU3 – OpenCL – FAHCore_18 
        - OpenCL compatible GPU, 5xxx series or newer*, see full list
        - 14.9 AMD device driver or newer
- GPU3 – OpenCL – FAHCore_21
        - OpenCL compatible GPU, 5xxx series or newer*, see full list
        - 15.1 AMD device driver or newer

Note: ATI/AMD (In beta testing, see Notes below)


Nvidia GPU Requirements
***********************
- GPU3 – OpenCL – FAHCore_17
        - OpenCL compatible GPU, 4xx series and above (Fermi, Kepler, Maxwell, and newer*)
        - 361.xx NV device driver or newer (327.xx is a known stable version for older GPUs)
- GPU3 – OpenCL – FAHCore_18
        - OpenCL compatible GPU, 4xx series and above (Fermi, Kepler, Maxwell, and newer*)
        - 361.xx NV device driver or newer (327.xx is a known stable version for older GPUs)
- GPU3 – OpenCL – FAHCore_21
        - OpenCL compatible GPU, 4xx series and above (Fermi, Kepler, Maxwell, and newer*)
        - 361.xx NV device driver (CUDA 8) or newer




Notes
-----
GPU drivers, models, features, and support develop very quickly. Please note these specific issues.

- Automatic updating of the GPUs.txt is now supported in V7.3.x and newer.
- See the Folding Support Forum New GPUs (whitelist/blacklist) section for more information about the GPU hardware (supported HW list, aka greylist) with newer GPUs.
- FAHCore_11, FAHCore_15, and FAHCore_16 are not supported in linux, and are going End Of Life.  FAHCore _11 EOL was announced in March 2011, and scheduled to end in September 2011.
- Folding on NV GPUs is currently limited to 64 bit distros.
- Several fahcore speed issues have been resolved in the latest NVidia driver, 361.xx or above.  However, support for older Tesla GPUs and older were dropped in this newer driver.
- Several fahcore speed issues have been resolved in the latest AMD driver, 15.x or above.  However, support for older GPUs were dropped in this newer driver.
- New GPU models with newer chip architecture may not be supported by the current software.  New fahcores and/or new drivers with updated optimizations may be required for full support.  New fahcores will not be available until some time after the new hardware products are sold to the public.  Then the fahcores and drivers may be updated, tested, and verified before released for folding.
- Folding on AMD GPUs is problematic in linux due to poor OpenCL driver suppport from AMD.
- Installing OEM specific GPU drivers can be problematic in Linux.  Please review the AMD GPU driver installation instructions for Linux.  Please review the NVidia GPU driverinstallation instructions for Linux.  See also this Folding Forum topic for tips installing the drivers.
