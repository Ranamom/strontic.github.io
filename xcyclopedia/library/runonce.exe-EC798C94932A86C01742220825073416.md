﻿---
title: runonce.exe | Run Once Wrapper
---

# runonce.exe 

* File Path: `C:\Windows\system32\runonce.exe`
* Description: Run Once Wrapper
* Comments: 

## Hashes

Type | Hash
-- | --
MD5 | `EC798C94932A86C01742220825073416`
SHA1 | `1478DC8635B564C740103C6A8FF5CAF8374DA0A0`
SHA256 | `5994E053D58DB049F4BAB2117C51CC314D1553BC6793FF000B232B66F709B0D7`
SHA384 | `C5CCED9623776636F0C0E586AEE2CF3DCCEB5D2BFD1621A3985C6C568609A72E1FBB3FE1643856DB83949F2FAA53D463`
SHA512 | `6B5CA46B74879732D8A147FBCB950CC7CD846264E05D5D7A27E25BB70CABF8451E68C564BDF02FE2BF33C3C885021252692D1A2ED8376F61022DAD87BCFDE524`
SSDEEP | `1536:vhMChceJibHnk/MkccqpyfDqsS92mqN1x7S9a1MvZ5v/G:66OcqpyrSMBN11SAqRJu`

## Runtime Data

### Usage (stdout):
```Batchfile

```

### Usage (stderr):
```Batchfile

```

### Child Processes:


## Signature

* Status: Signature verified.
* Serial: `3300000266BD1580EFA75CD6D3000000000266`
* Thumbprint: `A4341B9FD50FB9964283220A36A1EF6F6FAA7840`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: RUNONCE.EXE.MUI
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.19041.1 (WinBuild.160101.0800)
* Product Version: 10.0.19041.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.


## Possible Misuse

*The following table contains possible examples of `runonce.exe` being misused. While `runonce.exe` is **not** inherently malicious, its legitimate functionality can by abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[sigma](https://github.com/Neo23x0/sigma) | [godmode_sigma_rule.yml](https://github.com/Neo23x0/sigma/blob/master/other/godmode_sigma_rule.yml) | `            - '\Microsoft\Windows\CurrentVersion\RunOnce\'   # persistence` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_query_registry.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_query_registry.yml) | `            - 'currentVersion\runOnce'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_direct_asep_reg_keys_modification.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_direct_asep_reg_keys_modification.yml) | `            - '\software\Microsoft\Windows\CurrentVersion\RunOnce'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [sysmon_asep_reg_keys_modification.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/registry_event/sysmon_asep_reg_keys_modification.yml) | `            - '\software\Microsoft\Windows\CurrentVersion\RunOnce'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [sysmon_susp_run_key_img_folder.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/registry_event/sysmon_susp_run_key_img_folder.yml) | `            - '*\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce\\*'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [sysmon_asep_reg_keys_modification.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/sysmon/sysmon_asep_reg_keys_modification.yml) | `            - '\software\Microsoft\Windows\CurrentVersion\RunOnce'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [sysmon_suspicious_remote_thread.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/sysmon/sysmon_suspicious_remote_thread.yml) | `            - '\runonce.exe'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [sysmon_susp_run_key_img_folder.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/sysmon/sysmon_susp_run_key_img_folder.yml) | `            - '*\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce\\*'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Runonce.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Runonce.yml) | `Name: Runonce.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Runonce.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Runonce.yml) | `  - Command: Runonce.exe /AlternateShellStartup` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Runonce.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Runonce.yml) | `  - Path: C:\Windows\System32\runonce.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Runonce.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Runonce.yml) | `  - Path: C:\Windows\SysWOW64\runonce.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Runonce.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Runonce.yml) | `  - Link: https://cmatskas.com/configure-a-runonce-task-on-windows/` | 
[malware-ioc](https://github.com/eset/malware-ioc) | [misp-dukes-operation-ghost-event.json](https://github.com/eset/malware-ioc/blob/master/dukes/misp-dukes-operation-ghost-event.json) | `                                "description": "Adding an entry to the \"run keys\" in the Registry or startup folder will cause the program referenced to be executed when a user logs in. (Citation: Microsoft Run Key) These programs will be executed under the context of the user and will have the account's associated permissions level.\n\nThe following run keys are created by default on Windows systems:\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</code>\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</code>\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</code>\n\nThe <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnceEx</code> is also available but is not created by default on Windows Vista and newer. Registry run key entries can reference programs directly or list them as a dependency. (Citation: Microsoft RunOnceEx APR 2018) For example, it is possible to load a DLL at logon using a \"Depend\" key with RunOnceEx: <code>reg add HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnceEx\\0001\\Depend /v 1 /d \"C:\\temp\\evil[.]dll\"</code> (Citation: Oddvar Moe RunOnceEx Mar 2018)\n\nThe following Registry keys can be used to set startup folder items for persistence:\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\User Shell Folders</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Shell Folders</code>\n* <code>HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Shell Folders</code>\n* <code>HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\User Shell Folders</code>\n\nAdversaries can use these configuration locations to execute malware, such as remote access tools, to maintain persistence through system reboots. Adversaries may also use [Masquerading](https://attack.mitre.org/techniques/T1036) to make the Registry entries look as if they are associated with legitimate programs.",` | [© ESET 2014-2018](https://github.com/eset/malware-ioc/blob/master/LICENSE)
[malware-ioc](https://github.com/eset/malware-ioc) | [misp_invisimole.json](https://github.com/eset/malware-ioc/blob/master/invisimole/misp_invisimole.json) | `                "description": "Adding an entry to the \"run keys\" in the Registry or startup folder will cause the program referenced to be executed when a user logs in. (Citation: Microsoft Run Key) These programs will be executed under the context of the user and will have the account's associated permissions level.\n\nThe following run keys are created by default on Windows systems:\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</code>\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</code>\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</code>\n\nThe <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnceEx</code> is also available but is not created by default on Windows Vista and newer. Registry run key entries can reference programs directly or list them as a dependency. (Citation: Microsoft RunOnceEx APR 2018) For example, it is possible to load a DLL at logon using a \"Depend\" key with RunOnceEx: <code>reg add HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnceEx\\0001\\Depend /v 1 /d \"C:\\temp\\evil[.]dll\"</code> (Citation: Oddvar Moe RunOnceEx Mar 2018)\n\nThe following Registry keys can be used to set startup folder items for persistence:\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\User Shell Folders</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Shell Folders</code>\n* <code>HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Shell Folders</code>\n* <code>HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\User Shell Folders</code>\n\nThe following Registry keys can control automatic startup of services during boot:\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunServicesOnce</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\RunServicesOnce</code>\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunServices</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\RunServices</code>\n\nUsing policy settings to specify startup programs creates corresponding values in either of two Registry keys:\n* <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Policies\\Explorer\\Run</code>\n* <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Policies\\Explorer\\Run</code>\n\nThe Winlogon key controls actions that occur when a user logs on to a computer running Windows 7. Most of these actions are under the control of the operating system, but you can also add custom actions here. The <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\Userinit</code> and <code>HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\Shell</code> subkeys can automatically launch programs.\n\nPrograms listed in the load value of the registry key <code>HKEY_CURRENT_USER\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows</code> run when any user logs on.\n\nBy default, the multistring BootExecute value of the registry key <code>HKEY_LOCAL_MACHINE\\System\\CurrentControlSet\\Control\\Session Manager</code> is set to autocheck autochk *. This value causes Windows, at startup, to check the file-system integrity of the hard disks if the system has been shut down abnormally. Adversaries can add other programs or processes to this registry value which will automatically launch at boot.\n\n\nAdversaries can use these configuration locations to execute malware, such as remote access tools, to maintain persistence through system reboots. Adversaries may also use [Masquerading](https://attack.mitre.org/techniques/T1036) to make the Registry entries look as if they are associated with legitimate programs.",` | [© ESET 2014-2018](https://github.com/eset/malware-ioc/blob/master/LICENSE)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/index.md) |   - Atomic Test #2: Reg Key RunOnce [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/index.md) |   - Atomic Test #3: PowerShell Registry RunOnce [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [windows-index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/windows-index.md) |   - Atomic Test #2: Reg Key RunOnce [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [windows-index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/windows-index.md) |   - Atomic Test #3: PowerShell Registry RunOnce [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1012.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1012/T1012.md) | reg query HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnce | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1012.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1012/T1012.md) | reg query HKCU\Software\Microsoft\Windows\CurrentVersion\RunOnce | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | * <code>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunOnce</code> | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | * <code>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\RunOnce</code> | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | - [Atomic Test #2 - Reg Key RunOnce](#atomic-test-2---reg-key-runonce) | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | - [Atomic Test #3 - PowerShell Registry RunOnce](#atomic-test-3---powershell-registry-runonce) | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | ## Atomic Test #2 - Reg Key RunOnce | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | RunOnce Key Persistence. | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | ## Atomic Test #3 - PowerShell Registry RunOnce | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | RunOnce Key Persistence via PowerShell | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | Upon successful execution, a new entry will be added to the runonce item in the registry. | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1547.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1547.001/T1547.001.md) | \| reg_key_path \| Path to registry key to update \| Path \| HKLM:&#92;Software&#92;Microsoft&#92;Windows&#92;CurrentVersion&#92;RunOnce\| | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)



MIT License. Copyright (c) 2020 Strontic.

