---
external help file: OpenApi.Pwsh.dll-Help.xml
Module Name: OpenApi.Pwsh
online version: https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Import-OpenApiDocument.md
schema: 2.0.0
---

# Import-OpenApiDocument

## SYNOPSIS

Imports OpenAPI documents as OpenApiDocument objects.

## SYNTAX

### ByPath (Default)
```
Import-OpenApiDocument [-Path] <String[]> [[-OpenApiName] <String>] [-ReaderSettings <OpenApiReaderSettings>]
 [-PassThru] [<CommonParameters>]
```

### ByUri
```
Import-OpenApiDocument [-Uri] <Uri[]> [[-OpenApiName] <String>] [-ReaderSettings <OpenApiReaderSettings>]
 [-PassThru] [<CommonParameters>]
```

## DESCRIPTION

Imports the OpenAPI documents written in JSON or YAML as OpenApiDocument objects.

## EXAMPLES

### Example 1

```powershell
Import-OpenApiDocument -Path $HOME\PetStore.json -OpenApiName PetStoreV1
```

Imports the `$HOME\PetStore.json` file as an OpenApiDocument object.
The name `PetStoreV1` is specified by `-OpenApiName` parameter.

### Example 2

```powershell
Import-OpenApiDocument -Path $HOME\PetStore.json
```

Imports the `$HOME\PetStore.json` file as an OpenApiDocument object without `-OpenApiName` parameter.
In this case, the name is "PetStore", generated automatically from the file name.

### Example 3

```powershell
Import-OpenApiDocument -Uri https://example.com/PetStore.json
```

Imports the JSON file from the URI `https://example.com/PetStore.json` as an OpenApiDocument object without `-OpenApiName` parameter.
In this case, the name is "PetStore", generated automatically from the last segment of the URL.

## PARAMETERS

### -OpenApiName

The name which is associated with the OpenAPI document to be imported.
The name will be used in various cases, for example, as the `-OpenApiName` parameter value of the `Get-OpenApiDocument` cmdlet.

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

### -PassThru

Returns the imported OpenApiDocument object.

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

### -Path

The local file path of the OpenAPI document to be imported.

```yaml
Type: String[]
Parameter Sets: ByPath
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReaderSettings

The settings used to import the OpenAPI document.

```yaml
Type: OpenApiReaderSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri

The URI of the OpenAPI document to be imported.

```yaml
Type: Uri[]
Parameter Sets: ByUri
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String[]

### System.Uri[]

## OUTPUTS

### Microsoft.OpenApi.Models.OpenApiDocument

## NOTES

## RELATED LINKS

[Get-OpenApiDocument](https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Get-OpenApiDocument.md)

[Show-OpenApiExternalDocs](https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Show-OpenApiExternalDocs.md)
