

# FreeToolCheckYoutubeThumbnailResponseChecksInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**key** | [**KeyEnum**](#KeyEnum) |  |  [optional] |
|**label** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | &#x60;check&#x60;: a format YouTube may accept but does not name. |  [optional] |
|**detail** | **String** | The value found and the requirement. |  [optional] |



## Enum: KeyEnum

| Name | Value |
|---- | -----|
| RATIO | &quot;ratio&quot; |
| WIDTH | &quot;width&quot; |
| FILE_SIZE | &quot;file_size&quot; |
| FORMAT | &quot;format&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PASS | &quot;pass&quot; |
| FAIL | &quot;fail&quot; |
| CHECK | &quot;check&quot; |



