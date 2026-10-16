

# FreeToolCalculateAspectRatioResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**ratio** | **String** | Simplified ratio, e.g. &#x60;4:5&#x60;. Decimal ratios stay as given. |  [optional] |
|**decimal** | **BigDecimal** | Width divided by height, 4 decimals. |  [optional] |
|**width** | **Integer** |  |  [optional] |
|**height** | **Integer** |  |  [optional] |
|**rounding** | [**FreeToolCalculateAspectRatioResponseRounding**](FreeToolCalculateAspectRatioResponseRounding.md) |  |  [optional] |
|**orientation** | [**OrientationEnum**](#OrientationEnum) |  |  [optional] |
|**matches** | [**List&lt;FreeToolCalculateAspectRatioResponseMatchesInner&gt;**](FreeToolCalculateAspectRatioResponseMatchesInner.md) | Social media image presets with the same ratio, else the nearest. |  [optional] |



## Enum: OrientationEnum

| Name | Value |
|---- | -----|
| LANDSCAPE | &quot;landscape&quot; |
| PORTRAIT | &quot;portrait&quot; |
| SQUARE | &quot;square&quot; |



