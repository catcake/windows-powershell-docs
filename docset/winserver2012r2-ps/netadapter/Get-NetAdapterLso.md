---
external help file: MSFT_NetAdapterLso.cdxml-help.xml
Module Name: NetAdapter
online version: 
schema: 2.0.0
title: Get-NetAdapterLso
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-10-29
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: ECBBCA96-A4FB-434F-A8AB-3C10C81329BE
---

# Get-NetAdapterLso

## SYNOPSIS
Gets the large send offload (LSO) properties of the network adapter.

## SYNTAX

### ByName (Default)
```
Get-NetAdapterLso [[-Name] <String[]>] [-IncludeHidden] [-CimSession <CimSession[]>] [-ThrottleLimit <Int32>]
 [-AsJob] [<CommonParameters>]
```

### ByInstanceID
```
Get-NetAdapterLso -InterfaceDescription <String[]> [-IncludeHidden] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Get-NetAdapterLso** cmdlet gets the state of large send offload (LSO) settings on the network adapter.
LSO is a technology where the work of segmenting data into network frames is performed by the network adapter instead of by the TCP/IP stack.
With LSO, TCP/IP sends very large data packets down to the network adapter driver and the network adapter hardware.
The network adapter breaks up the data into smaller network-sized frames.
This increases the speed of high-end send operations and decreases the processor usage of the computer, because the work is performed on the network adapter.

## EXAMPLES

### EXAMPLE 1
```
PS C:\>Get-NetAdapterLso -Name MyAdapter
```

This example gets the LSO properties of the network adapter named MyAdapter.

### EXAMPLE 2
```
PS C:\>Get-NetAdapterLso -Name MyAdapter | Format-List -Property *
```

This example displays all of the LSO properties of the network adapter named MyAdapter.

### EXAMPLE 3
```
PS C:\>Get-NetAdapterLso -Name * | Where-Object -FilterScript { $_.Enabled }
```

This example gets all of the network adapters with LSO enabled.

## PARAMETERS

### -AsJob
ps_cimcommon_asjob

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
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
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

### -IncludeHidden
Specifies both visible and hidden network adapters should be included.
By default only visible network adapters are included.
If a wildcard character is used in identifying a network adapter and this parameter has been specified, then the wildcard string is matched against both hidden and visible network adapters.

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

### -InterfaceDescription
Specifies the network adapter interface description.
For a physical network adapter this is typically the vendors name of the network adapter followed by a part number and description, such as `Contoso 12345 Gigabit Network Device`.

```yaml
Type: String[]
Parameter Sets: ByInstanceID
Aliases: ifDesc, InstanceID

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of the network adapter.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: ifAlias, InterfaceAlias

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Management.Infrastructure.CimInstance#ROOT/StandardCimv2/MSFT_NetAdapter LsoSettingData
The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

## NOTES

## RELATED LINKS

[Format-List](http://go.microsoft.com/fwlink/p/?LinkID=113302)

[Where-Object](http://go.microsoft.com/fwlink/p/?LinkID=113423)

[Disable-NetAdapterLso](./Disable-NetAdapterLso.md)

[Enable-NetAdapterLso](./Enable-NetAdapterLso.md)

[Set-NetAdapterLso](./Set-NetAdapterLso.md)
