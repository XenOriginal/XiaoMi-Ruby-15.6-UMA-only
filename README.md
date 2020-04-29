# XiaoMi-Ruby-15.6-UMA-only

## From Clover to Opencore

1. Use scripts unlock CFG and set DVMT

2. Press Space in OpenCore boot page, and then select Clean NVRAM entry

## Features

1. Opencore Bootloader and all Hotpatch ACPI tables

2. Unlock CFG and DVMT limit, more original to mac

3. 99% Hardware is perfect even FN-Backlight button

## Hardware

For a 99% perfect Hackintosh on Xiaomi-Ruby-15.6-UMA-only, you need do following things.

1. Replace Wireless Network Cards from Realtek to BCM94360CS2 - Necessary

2. Replace your monitor from 45% NTSC to 72% NTSC (N156HCE-EN1) - Optional

3. Replace your m2 ssd from SATA to NVME - Optional

4. Upgrade your memory - Optional

5. Buy a good bluetooth soundbar - Optional

## BIOS Setting

1. Set a bios password and disable scurity boot - Necessary

2. Use scripts unlock CFG and set DVMT - Recommend (You can roll back by restore bios setting)

    You can test in Opencore boot page

## Work not Well

1. Internal Speaker (Intel® Smart Sound Technology) 

    Laptops with Intel SST will not have anything connected through them (usually internal mic) work, as it is not supported. You can check with Device Manager on Windows.
  
2. Realtek SD Card Reader
 
    You can passthrough it to VirtualMachine, because it's a USB device!
    
3. Use Opencore to launch Windows. You can press CTRL+Enter and CTRL+Index to set default boot device in the picker. And Boot Windows by using F12 on MI Logo.

## Generate your own SMbios

  Platforminfo

  For setting up the SMBIOS info, we'll use CorpNewt's GenSMBIOS and ProperTree application. https://github.com/corpnewt/GenSMBIOS https://github.com/corpnewt/ProperTree

  Because of the KabyLake R, we'll choose the MacBookPro14,2 SMBIOS:

  Run GenSMBIOS, pick option 1 for downloading MacSerial and Option 3 for selecting out SMBIOS. This will give us an output similar to the following:

  Type: MacBookPro14,2

  Serial: C02WXAY2HV2N

  Board Serial: C02826303CDHRPC8C

  SmUUID: 88AA1336-8DF9-477A-A39F-03D016ED0809

  The order is Product | Serial | Board Serial (MLB)

  The Type part gets copied to Generic -> SystemProductName.

  The Serial part gets copied to Generic -> SystemSerialNumber.

  The Board Serial part gets copied to Generic -> MLB.

  The SmUUID part gets copied toto Generic -> SystemUUID.

  We set Generic -> ROM to either an Apple ROM (dumped from a real Mac), your NIC MAC address, or any random MAC address (could be just 6 random bytes, for this guide we'll use 11223300 0000. After install follow the Fixing iServices page on how to find your real MAC Address)

  Reminder that you want either an invalid serial or valid serial numbers but those not in use, you want to get a message back like: "Invalid Serial" or "Purchase Date not Validated"

  Apple Check Coverage page https://checkcoverage.apple.com/cn/zh/
  
## Current Status in OpenCore

  Limited theme

  Press Space in OpenCore boot page, and then select Clean NVRAM entry

  Need more testing...

## Help Wanted
  Opencore will use modified ACPI table to boot Windows, but SSDT-XTPD0.aml and ACPI patch "Rename TDP0 to XPD0" will confilicts with it. who can help modified it to fit opencore, both of these are Acpi info of trackpad.
 
