---
external help file: OpenApi.Pwsh.dll-Help.xml
Module Name: OpenApi.Pwsh
online version: https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Build-IrmParam.md
schema: 2.0.0
---

# Build-IrmParam

## SYNOPSIS

Builds a paramter for `Invoke-RestMethod` cmdlet.

## SYNTAX

```
Build-IrmParam [-OpenApiName] <String> [-OperationId] <String> [<CommonParameters>]
```

## DESCRIPTION

Builds a paramter for `Invoke-RestMethod` cmdlet to invoke an API defined in an OpenAPI document.
The parameter is a `[hashtable]`, which can be used as a splatting variable.

If the generated parameter is not suitable for your needs, edit the OpenAPI document and try it again.

The details of the build logic will be customizable in the future.

## EXAMPLES

### Example 1

```powershell
$params = Build-IrmParam -OpenApiName UserApi -OperationId GetUser
```

The generated `$params` is a `[hashtable]` containing the keys: `Uri` and `Method`.
The values of `Uri` and `Method` depend on the `UserApi`'s `GetUser` API definition.

The `$params` can be used as a splatting variable for `Invoke-RestMethod` cmdlet.
For example:

```powershell
Invoke-RestMethod @params -FollowRelLink
```

The `Invoke-RestMethod` accepts the `$params` as a splatting variable and `-FollowRelLink` as an additional switch.

## PARAMETERS

### -OpenApiName

The name of the OpenAPI document used to build a paramter for `Invoke-RestMethod` cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationId

The OperationId used to build a paramter for `Invoke-RestMethod` cmdlet.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Collections.Hashtable

## NOTES

## RELATED LINKS

[Import-OpenApiDocument](https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Import-OpenApiDocument.md)
