---
external help file: OpenApi.Pwsh.dll-Help.xml
Module Name: OpenApi.Pwsh
online version: https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Get-OpenApiDocument.md
schema: 2.0.0
---

# Get-OpenApiDocument

## SYNOPSIS

Gets OpenApiDocument objects.

## SYNTAX

```
Get-OpenApiDocument [[-OpenApiName] <String>] [<CommonParameters>]
```

## DESCRIPTION

Gets the OpenApiDocument objects imported by `Import-OpenApiDocument`.

## EXAMPLES

### Example 1

```powershell
Get-OpenApiDocument
```

Gets all the imported OpenApiDocument objects.

### Example 2

```powershell
Get-OpenApiDocument -OpenApiName PetStore
```

Gets the OpenApiDocument object imported by the name "PetStore".

## PARAMETERS

### -OpenApiName

The name which is associated with the OpenApiDocument to be returned.
The name is specified when importing the OpenApiDocument.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.OpenApi.Models.OpenApiDocument

## NOTES

## RELATED LINKS

[Import-OpenApiDocument](https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Import-OpenApiDocument.md)
