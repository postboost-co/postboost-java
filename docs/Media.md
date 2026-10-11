

# Media


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**uuid** | **UUID** |  |  |
|**name** | **String** |  |  |
|**mimeType** | **String** |  |  |
|**type** | [**TypeEnum**](#TypeEnum) |  |  |
|**url** | **URI** |  |  |
|**thumbUrl** | **URI** |  |  [optional] |
|**isVideo** | **Boolean** |  |  |
|**isProcessing** | **Boolean** | True while an uploaded video is still being converted. |  [optional] |
|**width** | **Integer** | Width in pixels, when stored. |  [optional] |
|**height** | **Integer** | Height in pixels, when stored. |  [optional] |
|**durationMs** | **Integer** | Video duration in milliseconds; null for images or videos not read yet. |  [optional] |
|**size** | **Integer** | File size in bytes. |  [optional] |
|**altText** | **String** |  |  [optional] |
|**folder** | [**MediaFolderRef**](MediaFolderRef.md) |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| IMAGE | &quot;image&quot; |
| VIDEO | &quot;video&quot; |
| GIF | &quot;gif&quot; |



