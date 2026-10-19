

# GetRemoteUploadStatus200Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**progress** | **Integer** | Percent done. It stays &#x60;0&#x60; until the file is stored and is &#x60;100&#x60; once &#x60;status&#x60; is &#x60;completed&#x60;, so poll on &#x60;status&#x60;. |  |
|**media** | [**Media**](Media.md) | Present when &#x60;status&#x60; is &#x60;completed&#x60; (absent if the item was deleted before this poll). |  [optional] |
|**error** | **String** | Why the download failed. Present when &#x60;status&#x60; is &#x60;failed&#x60;. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| DOWNLOADING | &quot;downloading&quot; |
| PROCESSING | &quot;processing&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |



