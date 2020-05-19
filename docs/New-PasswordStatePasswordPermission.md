---
external help file: passwordstate-management-help.xml
Module Name: passwordstate-management
online version: https://github.com/dnewsholme/PasswordState-Management/blob/master/docs/New-PasswordStatePassword.md
schema: 2.0.0
---

# New-PasswordStatePasswordPermission

## SYNOPSIS
Add permissions to a PasswordState passwords.

## SYNTAX

### All (Default)
```
New-PasswordStatePasswordPermission [-PasswordID] <Int32> [-Permission] <String>
 [[-ApplyPermissionsForUserID] <String>] [-Sort] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PermissionID
```
New-PasswordStatePasswordPermission [-PasswordID] <Int32> [-Permission] <String>
 [[-ApplyPermissionsForUserID] <String>] [-ApplyPermissionsForSecurityGroupID] <Nullable`1[]> [-Sort] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### PermissionName
```
New-PasswordStatePasswordPermission [-PasswordID] <Int32> [-Permission] <String>
 [[-ApplyPermissionsForUserID] <String>] [-ApplyPermissionsForSecurityGroupName] <String> [-Sort] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Add permissions to a PasswordState passwords.

## EXAMPLES

### Example 1
```powershell
PS C:\> New-PasswordStatePasswordPermission -PasswordID 1 -Permission A -ApplyPermissionsForUserID "domain\username"
```

Grant administrator permissions to the username on password with ID 1.

### Example 2
```powershell
PS C:\> New-PasswordStatePasswordPermission -PasswordID 1 -Permission V -ApplyPermissionsForSecurityGroupName "ReadOnlyGroup"
```

Grant view permissions to the group "ReadOnlyGroup" on password with ID 1.

## PARAMETERS

### -ApplyPermissionsForSecurityGroupID
The SecurityGroupID you wish to apply permissions for.  
You can only specify SecurityGroupID or SecurityGroupName, not both in the same call.

```yaml
Type: Nullable`1[]
Parameter Sets: PermissionID
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplyPermissionsForSecurityGroupName
The SecurityGroupID you wish to apply permissions for.  
You can only specify SecurityGroupID or SecurityGroupName, not both in the same call.

```yaml
Type: String
Parameter Sets: PermissionName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplyPermissionsForUserID
The UserID (name) you wish to apply permissions for. Format: 'domain\username'

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordID
Unique identifier for the Password.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Permission
Set permission for the password.  
A for Administrator, M for Modify or V for View permissions.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: M, V

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sort
Sort the response object (not available at the moment)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Int32

### System.String

### System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Management.Automation.SwitchParameter

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS