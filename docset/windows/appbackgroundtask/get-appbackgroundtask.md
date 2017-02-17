---
ms.mktglfcycl: manage
ms.sitesec: library
ms.author: brianlic
author: brianlic-msft
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: PS_BackgroundTask.cdxml-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: w10
ms.technology: powershell-windows
ms.topic: reference
online version: 
schema: 2.0.0
title: Get-AppBackgroundTask
ms.assetid: 937AA4D9-7BB6-45CF-9AB0-ED45BFEC1725
---

# Get-AppBackgroundTask

## SYNOPSIS
Gets background task information.

## SYNTAX

```
Get-AppBackgroundTask [-PackageFamilyName <String>] [-IncludeResourceUsage] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AppBackgroundTask** cmdlet gets background task information for a task specified in the *PackageFamilyName* parameter.
A background task performs an activity for an application, such as downloading a file.
You must have administrator access to get background task information.

## EXAMPLES

### Example 1: Display background tasks
```
PS C:\> Get-AppBackgroundTask -PackageFamilyName "Microsoft.BingSports_8wekyb3d8bbwe"
```

This command displays the registered background tasks that belong to the Microsoft.BingSports_8wekyb3d8bbwe package family.

### Example 2: Display background tasks with resource usage data
```
PS C:\> Get-AppBackgroundTask -PackageFamilyName "Microsoft.BingSports_8wekyb3d8bbwe" -IncludeResourceUsage
```

This command displays the registered background tasks that belong to the Microsoft.BingSports_8wekyb3d8bbwe package family, including detailed resource usage information.

### Example 3: Display all background tasks for a user
```
PS C:\> Get-AppBackgroundTask
```

This command displays all registered background tasks for the current user.

## PARAMETERS

### -AsJob
Runs the cmdlet as a background job. Use this parameter to run commands that take a long time to complete. 

The cmdlet immediately returns an object that represents the job and then displays the command prompt. 
You can continue to work in the session while the job completes. 
To manage the job, use the `*-Job` cmdlets. 
To get the job results, use the [Receive-Job](http://go.microsoft.com/fwlink/?LinkID=113372) cmdlet. 

For more information about Windows PowerShell background jobs, see [about_Jobs](http://go.microsoft.com/fwlink/?LinkID=113251).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a [New-CimSession](http://go.microsoft.com/fwlink/p/?LinkId=227967) or [Get-CimSession](http://go.microsoft.com/fwlink/p/?LinkId=227966) cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeResourceUsage
Indicates that the cmdlet displays detailed resource usage data for a background task.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: iru

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageFamilyName
Specifies the package family name for which to display background task information.

```yaml
Type: String
Parameter Sets: (All)
Aliases: pfn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Management.Infrastructure.CimInstance# MSFT_BackgroundTask[]

## NOTES

## RELATED LINKS

[Start-AppBackgroundTask](./Start-AppBackgroundTask.md)

[Unregister-AppBackgroundTask](./Unregister-AppBackgroundTask.md)
