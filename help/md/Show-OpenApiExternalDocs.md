---
external help file: OpenApi.Pwsh.dll-Help.xml
Module Name: OpenApi.Pwsh
online version: https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Show-OpenApiExternalDocs.md
schema: 2.0.0
---

# Show-OpenApiExternalDocs

## SYNOPSIS

Shows an external document of an API.

## SYNTAX

```
Show-OpenApiExternalDocs [-OpenApiName] <String> [[-OperationId] <String>] [-AsModel] [<CommonParameters>]
```

## DESCRIPTION

Shows an external document of an API in your browser or as an OpenApiExternalDocs object.

## EXAMPLES

### Example 1

```powershell
Show-OpenApiExternalDocs -OpenApiName PetStore
```

Shows the document of the PetStore in your browser.

### Example 2

```powershell
Show-OpenApiExternalDocs -OpenApiName PetStore -OperationId listPets
```

Shows the document of the PetStore's `listPets` API in your browser.

### Example 3

```powershell
Show-OpenApiExternalDocs -OpenApiName PetStore -OperationId listPets -AsModel
```

Gets the OpenApiExternalDocs object of the PetStore's `listPets` API by the `-AsModel` switch.

## PARAMETERS

### -AsModel

Returns the OpenApiExternalDocs object of the API.

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

### -OpenApiName

The OpenAPI document name of the external document.

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

The OperationId of the external document.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft.OpenApi.Models.OpenApiExternalDocs

## NOTES

## RELATED LINKS

[Import-OpenApiDocument](https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Import-OpenApiDocument.md)
