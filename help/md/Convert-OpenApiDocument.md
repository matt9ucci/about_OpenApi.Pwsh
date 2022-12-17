---
external help file: OpenApi.Pwsh.dll-Help.xml
Module Name: OpenApi.Pwsh
online version: https://github.com/matt9ucci/about_OpenApi.Pwsh/blob/main/help/md/Convert-OpenApiDocument.md
schema: 2.0.0
---

# Convert-OpenApiDocument

## SYNOPSIS

Converts an OpenApiDocument object and its JSON/YAML format.

## SYNTAX

### ModelToString (Default)
```
Convert-OpenApiDocument [-Model] <IOpenApiSerializable> [-Version <OpenApiSpecVersion>]
 [-Format <OpenApiFormat>] [-WriterSettings <OpenApiWriterSettings>] [<CommonParameters>]
```

### StringToModel
```
Convert-OpenApiDocument [-String] <String> [-ReaderSettings <OpenApiReaderSettings>] [<CommonParameters>]
```

### FragmentToModel
```
Convert-OpenApiDocument [-String] <String> -Type <Type> [-Version <OpenApiSpecVersion>]
 [-ReaderSettings <OpenApiReaderSettings>] [<CommonParameters>]
```

## DESCRIPTION

Converts an OpenApiDocument object to its JSON/YAML format and vice versa.
Some types of JSON/YAML data can be fragments.

## EXAMPLES

### Example 1

```powershell
Convert-OpenApiDocument -Model ([Microsoft.OpenApi.Models.OpenApiDocument]::new())
```

Converts the OpenApiDocument object to the default version and format.

### Example 2

```powershell
Convert-OpenApiDocument -Model ([Microsoft.OpenApi.Models.OpenApiDocument]::new()) -Version OpenApi2_0 -Format Yaml
```

Converts the OpenApiDocument object to the OpenAPI v2 YAML.

### Example 3

```powershell
Convert-OpenApiDocument -Model (
  [Microsoft.OpenApi.Models.OpenApiExternalDocs]@{
    Description = 'ExternalDocs Description'
    Url = 'https://example.com/ExternalDocs/Url'
  }
)
```

Converts the OpenApiExternalDocs object to the default version and format fragment.

### Example 4

```powershell
Convert-OpenApiDocument -String '
{
  "openapi": "3.0.1",
  "info": {
    "title": "Info Title",
    "version": "0.1.0"
  },
  "paths": { }
}'
```

Converts the JSON to the OpenApiDocument object.

### Example 5

```powershell
Convert-OpenApiDocument -String '
{
  "description": "ExternalDocs Description",
  "url": "https://example.com/ExternalDocs/Url"
}' -Type Microsoft.OpenApi.Models.OpenApiExternalDocs
```

Converts the JSON fragment to the OpenApiExternalDocs object.

## PARAMETERS

### -Format

The format of the OpenAPI document.

```yaml
Type: OpenApiFormat
Parameter Sets: ModelToString
Aliases:
Accepted values: Json, Yaml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Model

The object to be converted.

```yaml
Type: IOpenApiSerializable
Parameter Sets: ModelToString
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ReaderSettings

The settings used to convert JSON/YAML to model.

```yaml
Type: OpenApiReaderSettings
Parameter Sets: StringToModel, FragmentToModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -String

The JSON/YAML to be converted.

```yaml
Type: String
Parameter Sets: StringToModel, FragmentToModel
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Type

The type to which convert JSON/YAML fragment to model.

```yaml
Type: Type
Parameter Sets: FragmentToModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version

The OpenAPI specification version of the OpenAPI document.

```yaml
Type: OpenApiSpecVersion
Parameter Sets: ModelToString, FragmentToModel
Aliases:
Accepted values: OpenApi2_0, OpenApi3_0

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriterSettings

The settings used to convert model to JSON/YAML.

```yaml
Type: OpenApiWriterSettings
Parameter Sets: ModelToString
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

### Microsoft.OpenApi.Interfaces.IOpenApiSerializable

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
