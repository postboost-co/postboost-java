

# ImageEditInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**mediaUuid** | **UUID** | UUID of the source media item to edit |  |
|**prompt** | **String** | Describe what to change in the image |  |
|**maskUuid** | **UUID** | UUID of a mask image. Transparent areas will be edited. |  [optional] |
|**useBrandVoice** | **Boolean** | Append the workspace brand voice&#39;s visual tone to the edit prompt. Off by default because edits are literal instructions. |  [optional] |
|**aspectRatio** | [**AspectRatioEnum**](#AspectRatioEnum) |  |  [optional] |
|**count** | **Integer** |  |  [optional] |
|**quality** | [**QualityEnum**](#QualityEnum) |  |  [optional] |



## Enum: AspectRatioEnum

| Name | Value |
|---- | -----|
| _1_1 | &quot;1:1&quot; |
| _16_9 | &quot;16:9&quot; |
| _9_16 | &quot;9:16&quot; |
| _4_5 | &quot;4:5&quot; |



## Enum: QualityEnum

| Name | Value |
|---- | -----|
| STANDARD | &quot;standard&quot; |
| HD | &quot;hd&quot; |



