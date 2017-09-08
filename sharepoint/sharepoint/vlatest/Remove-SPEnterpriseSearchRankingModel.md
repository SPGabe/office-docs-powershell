---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/b52a90c9-aad4-4849-ba3d-0089ba2fde42(Office.15).aspx
schema: 2.0.0
---

# Remove-SPEnterpriseSearchRankingModel

## SYNOPSIS
Deletes a ranking model.

## SYNTAX

```
Remove-SPEnterpriseSearchRankingModel [-Identity] <RankingModelPipeBind> -Owner <SearchObjectOwner>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf]
```

## DESCRIPTION
This cmdlet deletes a specified ranking model.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE 1------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"

$owner = Get-SPEnterpriseSearchOwner -Level ssa

Remove-SPEnterpriseSearchRankingModel -Identity 8f6fd0bc-06f9-43cf-bbab-08c377e083f4 -SearchApplication $ssa -Owner $owner
```

This example removes the ranking model for the search service application with the identity 8f6fd0bc-06f9-43cf-bbab-08c377e083f4.

### ------------------EXAMPLE 1------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
$owner = Get-SPEnterpriseSearchOwner -Level ssa
Remove-SPEnterpriseSearchRankingModel -Identity 8f6fd0bc-06f9-43cf-bbab-08c377e083f4 -SearchApplication $ssa -Owner $owner
```

This example removes the ranking model for the search service application with the identity 8f6fd0bc-06f9-43cf-bbab-08c377e083f4.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2016)
```
C:\PS>$owner = Get-SPEnterpriseSearchOwner -Level ssa
$MyRanking = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application" | Get-SPEnterpriseSearchRankingModel -Owner $owner
Remove-SPEnterpriseSearchRankingModel -Identity $MyRanking -Owner $owner
```

This example removes the ranking model object MyRanking from the search service application Search Service Application.

## PARAMETERS

### -Identity
Specifies the ranking model to delete.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, or an instance of a valid RankingModel object.

```yaml
Type: RankingModelPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Owner
Specifies the scope where the ranking model is available.
The available scopes are: SSA, Tenant, Site Collection or Site.
A ranking model can be available in multiple scopes.

```yaml
Type: SearchObjectOwner
Parameter Sets: (All)
Aliases: o

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

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Specifies the search application that contains the ranking model.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

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

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/b52a90c9-aad4-4849-ba3d-0089ba2fde42(Office.15).aspx)
