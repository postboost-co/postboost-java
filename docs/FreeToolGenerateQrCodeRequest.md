

# FreeToolGenerateQrCodeRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**data** | **String** | The link or text to encode. |  |
|**utm** | [**FreeToolGenerateQrCodeRequestUtm**](FreeToolGenerateQrCodeRequestUtm.md) |  |  [optional] |
|**errorCorrection** | [**ErrorCorrectionEnum**](#ErrorCorrectionEnum) | How much of the code can be damaged and still scan: L 7%, M 15%, Q 25%, H 30%. |  [optional] |
|**size** | **Integer** | Width and height of the SVG in pixels. |  [optional] |
|**foreground** | **String** | Colour of the modules, #RRGGBB. |  [optional] |
|**background** | **String** | Background colour, #RRGGBB. |  [optional] |



## Enum: ErrorCorrectionEnum

| Name | Value |
|---- | -----|
| L | &quot;L&quot; |
| M | &quot;M&quot; |
| Q | &quot;Q&quot; |
| H | &quot;H&quot; |



