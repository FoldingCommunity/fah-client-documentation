============
Requirements
============

The new V7 software has the same basic hardware and operating system requirements as the previous clients. 
However, a few software specific requirements have changed to support newer features. Listed by slot type:

- CPU Slot Requirements

  - Windows XP SP3 or newer, 32 or 64 bit

    - Intel P4 1.4 GHz processor or newer, or AMD equivalent (modern multi-core processors recommended)
    - | A limited selection of Projects are available for single core processors, 
        as the End Of Life for single core projects was announced in August 2013
      | Projects for higher numbers of cores may require 64-bit and have shorter deadlines, generally requiring a client running at or close to 24/7

  - Broadband internet connection or faster

Note: Although Pande Group has yet to provide a list of software prerequisites, donors have reported three issues. 
First is that Microsoft .NET Framework is required by V7 FAHControl in Windows, and Windows XP does not include .NET Framework by default. 
`Microsoft .NET 2.0 <http://www.microsoft.com/en-us/download/details.aspx?id=1639>`_ or newer should be installed to support the V7 software in Windows XP. 
All newer versions of Windows already include a supported version of .NET by default. 
In addition, Windows XP needs the `2008 C++ Redistributable (32 bit) <http://www.microsoft.com/en-us/download/confirmation.aspx?id=29>`_ for the FAHClient to operate. 
And depending on your network configuration, IPv4 may need to be given priority over IPv6 using this `Microsoft Fix It <http://support.microsoft.com/kb/2533454>`_ tool.

- GPU Slot Requirements
  
  - Windows XP SP3 or newer for NVIDA GPUs, 32 or 64 bit (Windows XP support and 32 bit support is limited, use Windows 7 or newer, 
    and a 64 bit operating system for full support of all FAHCore types)
  - Windows Vista SP2 or newer for AMD GPUs, 32 or 64 bit (32 bit support is limited, use 64 bit for full support)
  - FAHClient running more than part time to meet shorter deadlines
  - Broadband internet connection or faster
  - 1 or more supported GPU video cards
  - ATI/AMD

    - (GPU3 – OpenCL – FAHCore_17)
      
      - OpenCL compatible GPU, 5xxx series or newer*, see full list
      - 13.6 AMD device driver or newer (14.4+ improves speed)

    - (GPU3 – OpenCL – FAHCore_18)

      - OpenCL compatible GPU, 5xxx series or newer*, see full list
      - 14.9 AMD device driver or newer

    - (GPU3 – OpenCL – FAHCore_21)

      - OpenCL compatible GPU, 5xxx series or newer*, see full list
      - 15.1 AMD device driver or newer

  - NVIDIA

    - (GPU3 – OpenMM – fahcore_15) - End Of Life announced Nov. 2013

      - CUDA supported GPU (8xxx series and above), see full list
      - 327.xx NV device driver or newer
      - Special client settings needed to fold these projects. Ask in the Folding Support Forum.

    - (GPU3 – OpenCL – fahcore_17)

      - OpenCL compatible GPU, 4xx series and above (Fermi, Kepler, Maxwell, or newer*)
      - 361.xx NV device driver (CUDA 8) or newer (327.xx is a known stable version for older GPUs)

    - (GPU3 – OpenCL – fahcore_18)

      - OpenCL compatible GPU, 4xx series and above (Fermi, Kepler, Maxwell, or newer*)
      - 361.xx NV device driver (CUDA 8) or newer (327.xx is a known stable version for older GPUs)

    - (GPU3 – OpenCL – fahcore_21)

      - OpenCL compatible GPU, 4xx series and above (Fermi, Kepler, Maxwell, or newer*)
      - 361.xx NV device driver (CUDA 8) or newer (327.xx is a known stable version for older GPUs)

Note: GPU drivers, models, features, and support develop very quickly. Please note these specific issues.

- The v11.12 AMD device driver is the last version to support OpenCL on Windows XP. 7xxx series boards and newer will need Windows Vista SP2 or newer.
- Automatic updating of the GPUs.txt is now supported in V7.3.x and newer. A FAHClient.exe restart is required.
- Several fahcore speed issues have been resolved in the latest NVidia driver, 361.xx or above. 
  However, support for older Tesla GPUs and older were dropped in this newer driver.
- Several fahcore speed issues have been resolved in the latest AMD driver, 15.x or above. 
  However, support for older GPUs were dropped in this newer driver.
- See the Folding Support Forum New GPUs (whitelist/blacklist) section for more information about the GPU hardware greylist (supported HW list) with newer GPUs.
- The end of support for ATI/AMD 4xxx series and below was announced in March 2011, and scheduled to end in September 2011. 
  The last of the AMD Fahcore_11 (GPU2) work units actually lasted until June 2012, more than a year after the original announcement.
- The end of support for NVidia 8xxx series (G80, G84, G86, G92, G98) was announced in August 2013, and scheduled to end a year or so later. 
  The last of the NVidia Fahcore_11 (GPU2) works units ended when that older work server broke down in September 2014, 
  more than a year after the original announcement.
- \*New GPU models with newer chip architecture may not be supported by the current software. 
  New fahcores and/or new drivers with updated optimizations may be required for full support. 
  New fahcores will not be available until some time after the new hardware products are sold to the public. 
  Then the fahcores and drivers may be updated, tested, and verified before released for folding.

Note: Under Windows, antivirus software can interfere with the Folding\@home client files and cause errors. 
We suggest configuring antivirus software to exclude the FAH client directory and especially the Work directory from the antivirus scanning list. 
This can be done by going into the exclusion list panel that every antivirus should have. 
The work subdirectory contains semi-random binary data and can confuse overly aggressive heuristic virus scanning.