

# GetRemoteUploadStatus200Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**media** | [**Media**](Media.md) | Present when status is complete. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| DOWNLOADING | &quot;downloading&quot; |
| COMPLETE | &quot;complete&quot; |
| FAILED | &quot;failed&quot; |



