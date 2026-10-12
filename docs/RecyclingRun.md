

# RecyclingRun


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**reason** | **String** | Why the run skipped or failed; on &#x60;created&#x60;, a note such as &#x60;x_skipped_identical_text&#x60;. |  |
|**sourcePostUuid** | **String** |  |  |
|**createdPostUuid** | **String** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| CREATED | &quot;created&quot; |
| SKIPPED | &quot;skipped&quot; |
| FAILED | &quot;failed&quot; |



