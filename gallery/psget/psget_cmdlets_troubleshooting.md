---
description:  
manager:  carolz
ms.topic:  article
author:  jpjofre
ms.prod:  powershell
keywords:  powershell,cmdlet,gallery
ms.date:  2016-10-14
contributor:  manikb
title:  psget_cmdlets_troubleshooting
ms.technology:  powershell
---

## How to resolve "WARNING: Package 'your package name' failed to download" issue?




It is reported that Install-Module or Update-Module sometimes fails on some machines.
Based on our investigation, it is something to do with the networking connection.
Recently we updated NuGet provider so that it can reliably download packages.
You can follow the instructions below to install the latest build of NuGet provider and then install or update your module.
Let's use 'Azure' module as an example below.

```powershell
Install-PackageProvider NuGet -MinimumVersion 2.8.5.206 -Force
Launch new PowerShell Console
Update-Module Azure -Verbose
```

