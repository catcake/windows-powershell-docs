---
external help file: PrintMgmt_Cmdlets.xml
online version: 
schema: 2.0.0
ms.assetid: 0E552072-0B57-4C15-A5E7-4004D45568F0
---

# Add-PrinterDriver

## SYNOPSIS
Installs a printer driver on the specified computer.

## SYNTAX

```
Add-PrinterDriver [-Name] <String> [[-InfPath] <String>] [-AsJob] [-CimSession <CimSession>]
 [-ComputerName <String>] [-PrinterEnvironment <String>] [-ThrottleLimit <Int32>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
The **Add-PrinterDriver** cmdlet installs a printer driver on the specified computer.

You cannot use wildcard characters with **Add-PrinterDriver**.
You can use **Add-PrinterDriver** in a Windows PowerShell remoting session.

You need administrator privileges to use **Add-PrinterDriver**.

## EXAMPLES

### -------------------------- EXAMPLEExample 1: Add a printer driver with specified Driver Name -------------------------- 
Example: Add a printer driver
```
PS C:\> Add-PrinterDriver -Name "Driver Name"
```

This command installs the printer driver specified by **Name** on the local computer.

### -------------------------- ExampleXAMPLE 2: Add a printer driver with specified Driver Name on remote computer -------------------------- 
xample: Add a printer driver on remote computer
```
PS C:\> Add-PrinterDriver -Name "Driver Name" -ComputerName "printServer"
```

This command installs the printer driver specified by **Name** on the remote computer specified by **ComputerName**.

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
Type: CimSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Specifies the name of the computer on which to install the printer driver.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InfPath
Specifies the path to the printer driver INF file in the driver store.
INF files contain information about the printer and the printer driver.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the printer driver.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrinterEnvironment
Specifies the printer driver environment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### 
This cmdlet takes no input objects.

## OUTPUTS

### 
This cmdlet produces no output.

## NOTES

## RELATED LINKS

[Get-PrinterDriver](./Get-PrinterDriver.md)

[Remove-PrinterDriver](./Remove-PrinterDriver.md)
