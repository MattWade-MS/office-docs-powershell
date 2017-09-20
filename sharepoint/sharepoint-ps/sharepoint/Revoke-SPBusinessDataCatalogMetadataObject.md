---
external help file: 
applicable: SharePoint Server 2013, SharePoint Server 2016
schema: 2.0.0
---

# Revoke-SPBusinessDataCatalogMetadataObject

## SYNOPSIS
**Below Content Applies To:**SharePoint Server 2013

Applies to:

**Below Content Applies To:**SharePoint Server 2016

Revokes a right to a principal in the specified Business Data Connectivity Metadata Store metadata object.



## SYNTAX

```
Revoke-SPBusinessDataCatalogMetadataObject -Identity <MetadataObject> -Principal <SPClaim> -Right <PSBdcRight>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-SettingId <String>] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The Revoke-SPBusinessDataCatalogMetadataObject cmdlet revokes a right granted to a principal user in the specified Business Data Connectivity Metadata Store metadata object.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
C:\PS>$claimJohn = New-SPClaimsPrincipal -Identity "CONTOSO\johndoe" -IdentityType WindowsSamAccountName

C:\PS>$MetadataObject = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "LobSystem" -ServiceContext http://contoso -Name "ContosoDatabase"

C:\PS>Revoke-SPBusinessDataCatalogMetadataObject -Identity $MetadataObject -Principal $claimJohn -Right "Execute"
```

This example removes the execute right from the External System with the name ContosoDatabase for the user with the identity of johndoe on the domain CONTOSO.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$claimJohn = New-SPClaimsPrincipal -Identity "CONTOSO\johndoe" -IdentityType WindowsSamAccountName

C:\PS>$MetadataObject = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "LobSystem" -ServiceContext http://contoso -Name "ContosoDatabase"

C:\PS>Revoke-SPBusinessDataCatalogMetadataObject -Identity $MetadataObject -Principal $claimJohn -Right "Execute"
```

This example removes the execute right from the External System with the name ContosoDatabase for the user with the identity of johndoe on the domain CONTOSO.

## PARAMETERS

### -Identity
Specifies the Business Data Connectivity Metadata Store metadata object that contains the principal.

```yaml
Type: MetadataObject
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Principal
Specifies the principal to whom the rights apply.

The type must be a claim.

```yaml
Type: SPClaim
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Right
Specifies the right to revoke the principal.

The type must be one of the following valid PSBdcRight object types: All, Execute, Edit, SetPermissions, or SelectableInClients.

```yaml
Type: PSBdcRight
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingId
Specifies the custom environment settings model slice for which to revoke the right.

The type must be a valid string that identifies a model slice; for example, ModelSlice1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Server 2013, SharePoint Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
