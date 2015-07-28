Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18094

This directory contains the Win32 binaries.

Build Date:       Tue, 28 Jul 2015 03:18:22 Pacific Daylight Time
Last Changed Rev: 18090

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18094
 *BootSectImage Version 0.1 Build 18094
  Ecc.exe Version 0.01 Build 17712
 *EfiLdrImage Version 0.1 Build 18094
 *EfiRom Version 0.1 Build 18094
 *GenBootSector Version 0.2 Build 18094
 *GenCrc32 Version 0.2 Build 18094
 *GenDepex.exe Version 0.04 Build 18094
 *GenFds.exe 1.0 Build 18094
 *GenFfs Version 0.1 Build 18094
 *GenFv Version 0.1 Build 18094
 *GenFw Version 0.2 Build 18094
 *GenPage Version 0.2 Build 18094
 *GenPatchPcdTable.exe Version 0.10 Build 18094
 *GenSec Version 0.1 Build 18094
 *GenVtf Version 0.1 Build 18094
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 18094
  LzmaF86Compress Version 0.2 Build 18094
 *PatchPcdValue.exe Version 0.10 Build 18094
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 0.1 Build 18094
 *TargetTool.exe Version 0.01 Build 18094
 *TianoCompress Version 0.1 Build 18094
 *Trim.exe Version 0.10 Build 18094
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
 *VfrCompile version  2.00 (UEFI 2.4) Build 18094
 *VolInfo Version 0.83 Build 18094, Jul 28 2015
 *build.exe Version 0.60 Build 18094

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/28/2015 3:18:23AM Engine version = 5700.7163
  7/28/2015 3:18:23AM AntiVirus DAT version = 7875.0
  7/28/2015 3:18:23AM Number of detection signatures in EXTRA.DAT = None
  7/28/2015 3:18:23AM Names of detection signatures in EXTRA.DAT = None
  7/28/2015 3:18:23AM Scan Started On-Demand Scan
  7/28/2015 3:18:29AM Scan Summary
  7/28/2015 3:18:29AM Processes scanned : 0
  7/28/2015 3:18:29AM Processes detected : 0
  7/28/2015 3:18:29AM Processes cleaned : 0
  7/28/2015 3:18:29AM Boot sectors scanned : 2
  7/28/2015 3:18:29AM Boot sectors detected: 0
  7/28/2015 3:18:29AM Boot sectors cleaned : 0
  7/28/2015 3:18:29AM Files scanned : 71
  7/28/2015 3:18:29AM Files with detections: 0
  7/28/2015 3:18:29AM File detections : 0
  7/28/2015 3:18:29AM Files cleaned : 0
  7/28/2015 3:18:29AM Files deleted : 0
  7/28/2015 3:18:29AM Files not scanned : 0
  7/28/2015 3:18:29AM Scan Summary (Registry Scanning)
  7/28/2015 3:18:29AM Keys scanned : 0
  7/28/2015 3:18:29AM Keys detected : 0
  7/28/2015 3:18:29AM Keys cleaned : 0
  7/28/2015 3:18:29AM Keys deleted : 0
  7/28/2015 3:18:29AM Run time : 0:00:06
  7/28/2015 3:18:29AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18063:HEAD Source
------------------------------------------------------------------------  r18077 | abiesheuvel | 2015-07-27 06:49:54 -0700 (Mon, 27 Jul 2015) | 18 lines
  BaseTools/GenFw: move .debug contents to .data to save space
  In order to reduce the memory footprint of PE/COFF images when
  using large values for the PE/COFF section alignment, move the
  contents of the .debug section to data, and point the debug data
  directory entry to it. This allows us to drop the .debug section
  entirely, as well as any associated rounding. Since our .debug
  section only contains the filename of the ELF input image, the
  penalty of keeping this data in a non-discardable section is
  negligible.
  Note that the PE/COFF spec v6.3 explicitly mentions that this is
  allowed.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r18078 | abiesheuvel | 2015-07-27 06:50:09 -0700 (Mon, 27 Jul 2015) | 19 lines
  BaseTools/GenFw: move PE/COFF header closer to payload
  The secondary header (not the DOS header) of a PE/COFF binary
  does not reside at a fixed offset. Instead, its offset into the
  file is recorded in the DOS header.
  This gives us the flexibility to move it, along with the section
  headers, to right before the first section if there is considerable
  space before it, i.e., when the PE/COFF file alignment is substantially
  larger than the size of the header.
  Since the PE/COFF to TE conversion replaces everything before the
  section headers with a simple TE header, this change removes all
  the header padding from such images, leading to smaller files.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r18079 | abiesheuvel | 2015-07-27 06:50:19 -0700 (Mon, 27 Jul 2015) | 15 lines
  BaseTools: use GUID identifiable section for FFS alignment padding
  Instead of using an anonymous section of type EFI_SECTION_RAW to pad
  out the first aligned FFS section to its required alignment, use a
  section with a dedicated GUID if the size of the padding permits it.
  This allows for more flexibility when placing such FFS images in a
  firmware volume, because we will now be able to remove padding rather
  than add more, by shrinking the size of this section instead of
  padding out the start of the FFS image to file alignment.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r18080 | abiesheuvel | 2015-07-27 06:50:30 -0700 (Mon, 27 Jul 2015) | 19 lines
  BaseTools/GenFv: optimize away redundant padding
  To prevent double padding of XIP modules leading to excessive
  waste of FV space, try to adjust existing padding rather than
  adding more.
  Instead of adding a pad file to the FV to line up an FFS file that
  itself may contain padding to line up the payload, try to find a
  dedicated padding section inside the FFS, and reduce its size to
  place all subsequent aligned FFS section at their respective minimum
  alignments.
  When using 4 KB section alignment (which is required on AARCH64 in
  some cases), this will save 4 KB for each XIP module.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r18090 | yingke | 2015-07-27 22:53:08 -0700 (Mon, 27 Jul 2015) | 9 lines
  BaseTools: Add a keyword FvNameString in FDF
  The keyword with value TRUE OR FALSE is used to
  indicate whether the FV UI name is included in
  FV EXT header as a entry or not.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------