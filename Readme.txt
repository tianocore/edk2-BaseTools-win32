Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26005

This directory contains the Win32 binaries.

Build Date:       Mon, 25 Dec 2017 01:46:57 Pacific Standard Time
Last Changed Rev: 26000

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26005
 *BootSectImage Version 1.0 Build Build 26005
 *Brotli Version 0.5.2 Build 26005
 *Brotli Version 0.5.2 Build 26005
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 26005
 *EfiRom Version 0.1 Build 26005
 *GenBootSector Version 0.2 Build 26005
 *GenCrc32 Version 0.2 Build 26005
 *GenDepex.exe Version 0.04 Build 26005
 *GenFds.exe 1.0 Build 26005
 *GenFfs Version 0.1 Build 26005
 *GenFv Version 0.1 Build 26005
 *GenFw Version 0.2 Build 26005
 *GenPage Version 0.2 Build 26005
 *GenPatchPcdTable.exe Version 0.10 Build 26005
 *GenSec Version 0.1 Build 26005
 *GenVtf Version 0.1 Build 26005
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26005
  LzmaF86Compress Version 0.2 Build 26005
 *PatchPcdValue.exe Version 0.10 Build 26005
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 26005
 *TargetTool.exe Version 0.01 Build 26005
 *TianoCompress Version 0.1 Build 26005
 *Trim.exe Version 0.10 Build 26005
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26005
 *VolInfo Version 1.0 Build Build 26005
 *build.exe Version 0.60 Build 26005

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/25/2017 1:46:58AM Engine version = 5900.7806
  12/25/2017 1:46:58AM AntiVirus DAT version = 8755.0
  12/25/2017 1:46:58AM Number of detection signatures in EXTRA.DAT = None
  12/25/2017 1:46:58AM Names of detection signatures in EXTRA.DAT = None
  12/25/2017 1:46:58AM Scan Started On-Demand Scan
  12/25/2017 1:47:07AM Scan Summary
  12/25/2017 1:47:07AM Processes scanned : 0
  12/25/2017 1:47:07AM Processes detected : 0
  12/25/2017 1:47:07AM Processes cleaned : 0
  12/25/2017 1:47:07AM Boot sectors scanned : 2
  12/25/2017 1:47:07AM Boot sectors detected: 0
  12/25/2017 1:47:07AM Boot sectors cleaned : 0
  12/25/2017 1:47:07AM Files scanned : 81
  12/25/2017 1:47:07AM Files with detections: 0
  12/25/2017 1:47:07AM File detections : 0
  12/25/2017 1:47:07AM Files cleaned : 0
  12/25/2017 1:47:07AM Files deleted : 0
  12/25/2017 1:47:07AM Files not scanned : 0
  12/25/2017 1:47:07AM Scan Summary (Registry Scanning)
  12/25/2017 1:47:07AM Keys scanned : 0
  12/25/2017 1:47:07AM Keys detected : 0
  12/25/2017 1:47:07AM Keys cleaned : 0
  12/25/2017 1:47:07AM Keys deleted : 0
  12/25/2017 1:47:07AM Run time : 0:00:09
  12/25/2017 1:47:07AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25982:HEAD Source
------------------------------------------------------------------------  r25982 | edk2buildsystem | 2017-12-24 18:00:08 -0800 (Sun, 24 Dec 2017) | 7 lines
  BaseTools/GenSec: Fix potential null pointer dereference
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c40dbe5e7bf9f3f841d4f1c717c245e99854b786)

------------------------------------------------------------------------  r25983 | edk2buildsystem | 2017-12-25 01:36:13 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Update Makefile to work at absolute path
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 84e076c861ef21931b9d6eb9e0ab6206f1ddb0b8)

------------------------------------------------------------------------  r25984 | edk2buildsystem | 2017-12-25 01:36:21 -0800 (Mon, 25 Dec 2017) | 8 lines
  BaseTools: Add PcdValueCommon logic into C source CommonLib
  PcdValueCommon is used to calculate structure pcd value.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 309e37a22915dca12d3e5b914d8b3429f7624601)

------------------------------------------------------------------------  r25985 | edk2buildsystem | 2017-12-25 01:36:31 -0800 (Mon, 25 Dec 2017) | 10 lines
  BaseTools: Support Structure PCD value assignment in DEC/DSC
  https://bugzilla.tianocore.org/show_bug.cgi?id=542
  This is pure BaseTools enhancement to support PCD with one structure.
  User can specify PCD value based on its structure field.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ae7b6df816e913394a7f11264f24953658ff34ba)

------------------------------------------------------------------------  r25986 | edk2buildsystem | 2017-12-25 01:36:39 -0800 (Mon, 25 Dec 2017) | 11 lines
  BaseTools: Collect DynamicHii PCD values and assign it to VPD PCD Value
  https://bugzilla.tianocore.org/show_bug.cgi?id=661
  Collect all DynamicHii and DynamicExHii PCD value into PCD
  PcdNvStoreDefaultValueBuffer, then firmware can access this PCD value
  to get the variable default setting.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 34952f493c24c02f5eba6ae86ed758d3311cddb1)

------------------------------------------------------------------------  r25987 | edk2buildsystem | 2017-12-25 01:36:49 -0800 (Mon, 25 Dec 2017) | 9 lines
  BaseTools: Support Structure PCD value inherit between the different SKUs
  https://bugzilla.tianocore.org/show_bug.cgi?id=543
  Structure PCD field value can inherit between the different SKUIds.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8518bf0b92a78938341a2752a0044f04336668cc)

------------------------------------------------------------------------  r25988 | edk2buildsystem | 2017-12-25 01:36:58 -0800 (Mon, 25 Dec 2017) | 33 lines
  BaseTools: PcdDataBase Optimization for multiple SkuIds
  https://bugzilla.tianocore.org/show_bug.cgi?id=546
  BaseTools will generate the optimized PCD database to save the image size
  at build time for multiple SKUs. The optimized PCD database layout will be like
  below, the PCD database will be composed of the full default SKU data
  (PCD_DATABASE_INIT) and the non-default SKU delta data(PCD_DATABASE_SKU_DELTA).
  PCD driver will build HOB to store the full default SKU data, and patch HOB
  data based on non-default SKU delta data for the SKU set by SetSku(),
  it can save memory resource at boot time.
  //
  // PCD database layout:
  // +---------------------------------+
  // | PCD_DATABASE_INIT (DEFAULT SKU) |
  // +---------------------------------+
  // | PCD_DATABASE_SKU_DELTA (SKU A)  |
  // +---------------------------------+
  // | PCD_DATABASE_SKU_DELTA (SKU B)  |
  // +---------------------------------+
  // | ......                          |
  // +---------------------------------+
  //
  BaseTools, PCD database and driver updates are needed for this proposal.
  For single SKU (default) case, this proposal is expected to have no impact.
  For multi-SKU case, PCD database format will be changed.
  So, PcdDataBase Version is also updated from 6 to 7.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2b8a6c44e0deb508f79804dd5ff7156bc7e25493)

------------------------------------------------------------------------  r25989 | edk2buildsystem | 2017-12-25 01:37:06 -0800 (Mon, 25 Dec 2017) | 11 lines
  BaseTools: Report Structure PCD value and SKU, DefaultStore info
  https://bugzilla.tianocore.org/show_bug.cgi?id=706
  Add Structure PCD support for Build report. Structure PCD field value described
  in DEC/DSC will be display in build report. And, PCD value for each SKU and
  Default store will also be shown in build report.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e651d06c5ed167e706e2dbe122ec0953a54033f3)

------------------------------------------------------------------------  r25990 | edk2buildsystem | 2017-12-25 01:37:13 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Update NV Default Header format to include the max size
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@Intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 47854fd598b73267d57594c5bac6a2326332b08c)

------------------------------------------------------------------------  r25991 | edk2buildsystem | 2017-12-25 01:37:19 -0800 (Mon, 25 Dec 2017) | 8 lines
  BaseTools: Update SkuId as SKU_ID type to follow current implementation
  Update PCD DB and Default setting format as nature alignment.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7e6e459a3d91c07db1f97258aec323a982375e19)

------------------------------------------------------------------------  r25992 | edk2buildsystem | 2017-12-25 01:37:25 -0800 (Mon, 25 Dec 2017) | 10 lines
  BaseTools: Optimize VPD PCD value for the different SKUs
  If VPD PCD value is same in the different SKUs, the different SKUs will
  save the same offset for this PCD in VPD region. That means there is only
  one PCD value copy in VPD region to save VPD space.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 626bece451db2e2a19fa7696889ad4d4c441b16e)

------------------------------------------------------------------------  r25993 | edk2buildsystem | 2017-12-25 01:37:31 -0800 (Mon, 25 Dec 2017) | 9 lines
  BaseTools: Fixed the issue of Multiple Skus are always disables
  When multiple skus are enabled, PCD database should record the supported SKUs.
  This patch fixes PCD database to add the missing supported SKUs.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@Intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 65eff519e5ef56ddf51b11ed3524f55854e49dde)

------------------------------------------------------------------------  r25994 | edk2buildsystem | 2017-12-25 01:37:37 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Add error message if Structure PCD value is wrong
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b23957242c01ae776af86f91ebb35827422dec60)

------------------------------------------------------------------------  r25995 | edk2buildsystem | 2017-12-25 01:37:43 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Generate correct VPD PCD value to store the default setting
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0b6c5954e1d9a17e01eee7d5ef840a5b4790e2e8)

------------------------------------------------------------------------  r25996 | edk2buildsystem | 2017-12-25 01:37:48 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Correct PCD generation logic to make sure DB is use
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 67e63e9a7b3620fc5fdd3df61b4477a8cd5bc944)

------------------------------------------------------------------------  r25997 | edk2buildsystem | 2017-12-25 01:37:53 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Check PCD DataType and the maxsize.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 520365decb26e5176ec2bb614f11ddeaa495de54)

------------------------------------------------------------------------  r25998 | edk2buildsystem | 2017-12-25 01:37:59 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Support nest field name in DSC/DEC
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a09395932d997d41f59ae3ee2f7f77f91f5caa02)

------------------------------------------------------------------------  r25999 | edk2buildsystem | 2017-12-25 01:38:05 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Fix VPD data optimization issue
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8ac167890f2a8ef4918586e7e94190c52d59a4cc)

------------------------------------------------------------------------  r26000 | edk2buildsystem | 2017-12-25 01:38:09 -0800 (Mon, 25 Dec 2017) | 6 lines
  BaseTools: Fixed the issue of structure pcd filed sku inherit override
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c05c2c0526aadb0bc9ff0939bab1dec21c41c3ef)

------------------------------------------------------------------------