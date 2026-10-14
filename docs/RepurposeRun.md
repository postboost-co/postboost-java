

# RepurposeRun


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**runId** | **Integer** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**error** | **String** | Why the run failed. |  |
|**postUuid** | **UUID** | The draft post, once created. |  |
|**creditsUsed** | **Integer** |  |  |
|**result** | [**RepurposeResult**](RepurposeResult.md) |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| QUEUED | &quot;queued&quot; |
| RUNNING | &quot;running&quot; |
| OK | &quot;ok&quot; |
| PARTIAL | &quot;partial&quot; |
| FAILED | &quot;failed&quot; |



