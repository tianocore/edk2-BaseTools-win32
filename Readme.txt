Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17702

This directory contains the Win32 binaries.

Build Date:       Wed, 24 Jun 2015 03:16:48 Pacific Daylight Time
Last Changed Rev: 17696

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17702
 *BootSectImage Version 0.1 Build 17702
  Ecc.exe Version 0.01 Build 17553
 *EfiLdrImage Version 0.1 Build 17702
 *EfiRom Version 0.1 Build 17702
 *GenBootSector Version 0.2 Build 17702
 *GenCrc32 Version 0.2 Build 17702
 *GenDepex.exe Version 0.04 Build 17702
 *GenFds.exe 1.0 Build 17702
 *GenFfs Version 0.1 Build 17702
 *GenFv Version 0.1 Build 17702
 *GenFw Version 0.2 Build 17702
 *GenPage Version 0.2 Build 17702
 *GenPatchPcdTable.exe Version 0.10 Build 17702
 *GenSec Version 0.1 Build 17702
 *GenVtf Version 0.1 Build 17702
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 17702
  LzmaF86Compress Version 0.2 Build 17702
 *PatchPcdValue.exe Version 0.10 Build 17702
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
 *Split Version 0.1 Build 17702
 *TargetTool.exe Version 0.01 Build 17702
 *TianoCompress Version 0.1 Build 17702
 *Trim.exe Version 0.10 Build 17702
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
 *VfrCompile version  2.00 (UEFI 2.4) Build 17702
 *VolInfo Version 0.83 Build 17702, Jun 24 2015
 *build.exe Version 0.60 Build 17702

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  6/24/2015 3:16:49AM Engine version = 5700.7163
  6/24/2015 3:16:49AM AntiVirus DAT version = 7841.0
  6/24/2015 3:16:49AM Number of detection signatures in EXTRA.DAT = None
  6/24/2015 3:16:49AM Names of detection signatures in EXTRA.DAT = None
  6/24/2015 3:16:49AM Scan Started On-Demand Scan
  6/24/2015 3:16:59AM Scan Summary
  6/24/2015 3:16:59AM Processes scanned : 0
  6/24/2015 3:16:59AM Processes detected : 0
  6/24/2015 3:16:59AM Processes cleaned : 0
  6/24/2015 3:16:59AM Boot sectors scanned : 2
  6/24/2015 3:16:59AM Boot sectors detected: 0
  6/24/2015 3:16:59AM Boot sectors cleaned : 0
  6/24/2015 3:16:59AM Files scanned : 71
  6/24/2015 3:16:59AM Files with detections: 0
  6/24/2015 3:16:59AM File detections : 0
  6/24/2015 3:16:59AM Files cleaned : 0
  6/24/2015 3:16:59AM Files deleted : 0
  6/24/2015 3:16:59AM Files not scanned : 0
  6/24/2015 3:16:59AM Scan Summary (Registry Scanning)
  6/24/2015 3:16:59AM Keys scanned : 0
  6/24/2015 3:16:59AM Keys detected : 0
  6/24/2015 3:16:59AM Keys cleaned : 0
  6/24/2015 3:16:59AM Keys deleted : 0
  6/24/2015 3:16:59AM Run time : 0:00:10
  6/24/2015 3:16:59AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17685:HEAD Source
------------------------------------------------------------------------  r17685 | bobfeng | 2015-06-23 01:45:06 -0700 (Tue, 23 Jun 2015) | 5 lines
  BaseTools/Build: Add error report for incorrect syntax in DEC file.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: "Bob Feng" <bob.c.feng@intel.com>
  Reviewed-by: Laszlo Ersek <lersek@redhat.com>

------------------------------------------------------------------------  r17686 | lgao4 | 2015-06-23 03:48:04 -0700 (Tue, 23 Jun 2015) | 8 lines
  BaseTools: Convert ".\\" to "" in FilePath
  Convert ".\\" to "", because it doesn't work with WINDOWS_EXTENSION_PATH.
  WINDOWS_EXTENSION_PATH can support the file path larger than 260 length.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r17692 | jljusten | 2015-06-23 16:34:09 -0700 (Tue, 23 Jun 2015) | 9 lines
  BaseTools/EdkLogger: Support unit tests with a SILENT log level
  This allows the unit tests to run without the errors logging to the
  screen.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jordan Justen <jordan.l.justen@intel.com>
  Reviewed-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r17694 | jljusten | 2015-06-23 16:34:19 -0700 (Tue, 23 Jun 2015) | 37 lines
  BaseTools/UniClassObject: Verify valid UCS-2 chars in UTF-16 .uni files
  Supplementary Plane characters can exist in UTF-16 files,
  but they are not valid UCS-2 characters.
  For example, refer to this python interpreter code:
  >>> import codecs
  >>> codecs.encode(u'\U00010300', 'utf-16')
  '\xff\xfe\x00\xd8\x00\xdf'
  Therefore the UCS-4 0x00010300 character is encoded as two
  16-bit numbers (0xd800 0xdf00) in a little endian UTF-16
  file.
  For more information, see:
  http://en.wikipedia.org/wiki/UTF-16#U.2B10000_to_U.2B10FFFF
  This means that our current BaseTools code could be allowing
  unsupported UTF-16 characters be used. To fix this, we decode the file
  using python's utf-16 decode support. Then we verify that each
  character's code point is 0xffff or less.
  v3:
  * Based on Mike Kinney's feedback, we now read the whole file and
  verify up-front that it contains valid UCS-2 characters. Thanks
  also to Laszlo Ersek for pointing out the Supplementary Plane
  characters.
  v4:
  * Reject code points in 0xd800-0xdfff range since they are reserved
  for UTF-16 surrogate pairs. (lersek)
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jordan Justen <jordan.l.justen@intel.com>
  Reviewed-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r17696 | jljusten | 2015-06-23 16:34:28 -0700 (Tue, 23 Jun 2015) | 27 lines
  BaseTools/UniClassObject: Support UTF-8 string data in .uni files
  This allows .uni input files to be encoded with UTF-8. Today, we only
  support UTF-16 encoding.
  The strings are still converted to UCS-2 data for use in EDK II
  modules. (This is the only unicode character format supported by UEFI
  and EDK II.)
  Although UTF-8 would allow any UCS-4 character to be present in the
  source file, we restrict the entire file to the UCS-2 range.
  (Including comments.) This allows the files to be converted to UTF-16
  if needed.
  v2:
  * Drop .utf8 extension. Use .uni file for UTF-8 data (mdkinney)
  * Merge in 'BaseTools/UniClassObject: Verify string data is 16-bit'
  commit
  v3:
  * Restrict the entire file's characters (including comments) to the
  UCS-2 range in addition to string data. (mdkinney)
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jordan Justen <jordan.l.justen@intel.com>
  Reviewed-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------