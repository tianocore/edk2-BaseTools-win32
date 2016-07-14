Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 21814

This directory contains the Win32 binaries.

Build Date:       Thu, 14 Jul 2016 03:11:07 Pacific Daylight Time
Last Changed Rev: 21783

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 21077
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 21077
 *GenFds.exe 1.0 Build 21814
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 21077
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 21077
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 21077
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 21077
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 21725

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/14/2016 3:11:09AM Engine version = 5700.7163
  7/14/2016 3:11:09AM AntiVirus DAT version = 8225.0
  7/14/2016 3:11:09AM Number of detection signatures in EXTRA.DAT = None
  7/14/2016 3:11:09AM Names of detection signatures in EXTRA.DAT = None
  7/14/2016 3:11:09AM Scan Started On-Demand Scan
  7/14/2016 3:11:18AM Scan Summary
  7/14/2016 3:11:18AM Processes scanned : 0
  7/14/2016 3:11:18AM Processes detected : 0
  7/14/2016 3:11:18AM Processes cleaned : 0
  7/14/2016 3:11:18AM Boot sectors scanned : 2
  7/14/2016 3:11:18AM Boot sectors detected: 0
  7/14/2016 3:11:18AM Boot sectors cleaned : 0
  7/14/2016 3:11:18AM Files scanned : 55
  7/14/2016 3:11:18AM Files with detections: 0
  7/14/2016 3:11:18AM File detections : 0
  7/14/2016 3:11:18AM Files cleaned : 0
  7/14/2016 3:11:18AM Files deleted : 0
  7/14/2016 3:11:18AM Files not scanned : 0
  7/14/2016 3:11:18AM Scan Summary (Registry Scanning)
  7/14/2016 3:11:18AM Keys scanned : 0
  7/14/2016 3:11:18AM Keys detected : 0
  7/14/2016 3:11:18AM Keys cleaned : 0
  7/14/2016 3:11:18AM Keys deleted : 0
  7/14/2016 3:11:18AM Run time : 0:00:10
  7/14/2016 3:11:18AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 21725:HEAD Source
------------------------------------------------------------------------  r21760 | edk2buildsystem | 2016-07-13 11:50:57 -0700 (Wed, 13 Jul 2016) | 10 lines
  BaseTools/GenFds: factor out Region.PadBuffer() method
  The same logic is used in five places; factor it out to a common method.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5588565f4845d8138888f436218bc8334c0be54f)

------------------------------------------------------------------------  r21761 | edk2buildsystem | 2016-07-13 11:51:03 -0700 (Wed, 13 Jul 2016) | 61 lines
  BaseTools/GenFds: speed up Region.PadBuffer()
  The current implementation calls both pack() and Buffer.write() Size
  times. The new implementation calls both of these methods only once; the
  full data to write are constructed locally [1]. The range() function is
  replaced by xrange() because the latter is supposed to be faster / lighter
  weight [2].
  On my laptop, I tested the change as follows: I pre-built the series at
  [3] with
  build -a X64 -p OvmfPkg/OvmfPkgX64.dsc -t GCC48 -b DEBUG \
  -D HTTP_BOOT_ENABLE -D SECURE_BOOT_ENABLE
  (The series at [3] is relevant because it increases the size of one of the
  padded regions by 8.5 MB, slowing down the build quite a bit.)
  With all source code already compiled, repeating the above command takes
  approximately 45 seconds. With the patch applied, it goes down to 29
  seconds.
  [1] http://stackoverflow.com/questions/27384093/fastest-way-to-write-huge-data-in-file
  [2] https://docs.python.org/2/library/functions.html?highlight=xrange#xrange
  [3] http://thread.gmane.org/gmane.comp.bios.edk2.devel/14214
  We can also measure the impact with a synthetic test:
  > import timeit
  >
  > test_old = """
  > import struct, string, StringIO
  > Size = (8 * 1024 + 512) * 1024
  > Buffer = StringIO.StringIO()
  > PadData = 0xFF
  > for i in range(0, Size):
  >     Buffer.write(struct.pack('B', PadData))
  > """
  >
  > test_new = """
  > import struct, string, StringIO
  > Size = (8 * 1024 + 512) * 1024
  > Buffer = StringIO.StringIO()
  > PadByte = struct.pack('B', 0xFF)
  > PadData = string.join(PadByte for i in xrange(0, Size))
  > Buffer.write(PadData)
  > """
  >
  > print(timeit.repeat(stmt=test_old, number=1, repeat=3))
  > print(timeit.repeat(stmt=test_new, number=1, repeat=3))
  The output is
  [8.231637001037598, 8.81188416481018, 8.948754072189331]
  [0.5503702163696289, 0.5461571216583252, 0.578315019607544]
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit bd907fb6386560e621112beca7b7d381d0003967)

------------------------------------------------------------------------  r21769 | edk2buildsystem | 2016-07-13 11:51:48 -0700 (Wed, 13 Jul 2016) | 20 lines
  BaseTools/GenFds: unbreak Region.PadBuffer
  In its current form, Region.PadBuffer() fills every second byte with 0x20,
  the default separator string of Python's string.join():
  https://docs.python.org/2/library/string.html#string.join
  This corrupts some firmware because (a) 0x20 never corresponds to any
  ErasePolarity, (b) the PadData produced are actually longer than Size.
  Cc: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reported-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Fixes: bd907fb6386560e621112beca7b7d381d0003967
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Tested-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  (cherry picked from commit a78b518b6eddef545fa440822bec315b31e4e987)

------------------------------------------------------------------------  r21783 | edk2buildsystem | 2016-07-14 02:06:09 -0700 (Thu, 14 Jul 2016) | 12 lines
  BaseTools: Update the FV region name as upper letter
  Since in the GenFds phase, the FV is generated as upper letter. This
  patch update the FV region name as upper letter, it can fix the build
  report generate failure on case sensitive file system.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Andrew Fish <afish@apple.com>
  (cherry picked from commit 0199377c0d634218d0e06478ca766b7d891651c5)

------------------------------------------------------------------------