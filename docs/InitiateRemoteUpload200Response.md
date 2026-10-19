

# InitiateRemoteUpload200Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | [**StatusEnum**](#StatusEnum) | &#x60;completed&#x60; and &#x60;failed&#x60; are final; &#x60;pending&#x60; means the file downloads in the background. |  |
|**media** | [**Media**](Media.md) | Present when &#x60;status&#x60; is &#x60;completed&#x60;. This copy has no &#x60;size&#x60;; &#x60;getMedia&#x60; returns it. |  [optional] |
|**error** | **String** | Why the download failed. Present when &#x60;status&#x60; is &#x60;failed&#x60;. |  [optional] |
|**downloadId** | **UUID** | Present when &#x60;status&#x60; is &#x60;pending&#x60;. Pass it to &#x60;getRemoteUploadStatus&#x60;. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |



