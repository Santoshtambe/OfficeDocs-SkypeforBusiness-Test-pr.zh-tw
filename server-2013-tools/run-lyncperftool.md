﻿---
title: Run LyncPerfTool
TOCTitle: Run LyncPerfTool
ms:assetid: f2fd1940-d744-47b5-b299-04a914039182
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/JJ945612(v=OCS.15)
ms:contentKeyID: 52056020
ms.date: 06/25/2014
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Run LyncPerfTool

 

_**上次修改主題的時間：** 2013-02-24_

Before running the Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe), you must create users, contacts, and scenarios. For details about using the tools to perform these actions, see [Create Users and Contacts](create-users-and-contacts.md) and [Configure User Profile](configure-user-profile.md). Running these tools will also generate a file that will run LyncPerfTool.exe as part of a batch file with the required parameters included.

## Running the Lync Server 2013 Stress and Performance Tool

The UserProfileGenerator.exe tool creates a batch file that enables you to run LyncPerfTool.exe by registering the LyncPerfTool performance counters and loading the XML configuration file. The batch file runs one instance of LyncPerfTool.exe per configuration file. To run the batch file, do the following:

1.  Copy the folder that contains the configuration folders and files to the directory that contains LyncStressTool.exe on each client computer. (For example, if you generated the configuration files in the folder named 1.28\_13.16.16, copy that folder to the folder that contains LyncPerfTool.exe on each client.)

2.  Navigate to the appropriately numbered client folder and run the RunClient batch script. You can simply double-click the batch file in Windows Explorer and it will run all of the configuration files for that client number. You can also run the script from the appropriate client folder by using the following syntax:
    
       ```Batch
        RunClient0.bat "C:\Program Files\Microsoft Lync Server 2013\LyncStressAndPerfTool\LyncStress" 
       ```

To run LyncPerfTool.exe directly, open a command prompt, and then type the following command at the command line (when doing this for the first time, be sure to register the performance counters regsvr32 /i /n /s LyncPerfToolPerf.dll, as show in the note later in this topic):LyncPerfTool.exe /file:\<configXML\>

```Powershell
LyncPerfTool.exe /file:IM_client0.xml
```

To have the tool display the values in the configuration file, include the /displayfile parameter on the preceding command, like this:

```Powershell
LyncPerfTool.exe /file:IM_client0.xml /displayfile
```

To end the process, press Ctrl+C.

<table>
<thead>
<tr class="header">
<th><img src="images/JJ945612.note(OCS.15).gif" title="note" alt="note" />附註：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Before running LyncPerfTool directly, you must register the performance counters. Enter the following command to register performance counters:</td>
</tr>
</tbody>
</table>


```Powershell
regsvr32 /i /n /s LyncPerfToolPerf.dll
```

<table>
<thead>
<tr class="header">
<th><img src="images/JJ945612.note(OCS.15).gif" title="note" alt="note" />附註：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Every instance of LyncPerfTool.exe that you start will immediately start signing in users, usually at a rate of one user per second. The peak user sign-in rate for the pool is about 12 per second. This means that you should not start more than 12 LyncPerfTool instances at the same time, while the users are still signing in. 1000 users will take about 20 minutes to fully sign in, at one per second.</td>
</tr>
</tbody>
</table>


## 請參閱

#### 概念

[Create Users and Contacts](create-users-and-contacts.md)  
[Configure User Profile](configure-user-profile.md)

