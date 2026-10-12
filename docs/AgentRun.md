

# AgentRun


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** |  |  |
|**agentUuid** | **UUID** |  |  |
|**agentType** | **String** |  |  |
|**trigger** | [**TriggerEnum**](#TriggerEnum) |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**startedAt** | **OffsetDateTime** |  |  [optional] |
|**finishedAt** | **OffsetDateTime** |  |  [optional] |
|**itemsChecked** | **Integer** |  |  |
|**proposalsCreated** | **Integer** |  |  |
|**creditsUsed** | **Integer** | AI credits this run used. |  |
|**summary** | **String** |  |  [optional] |
|**error** | **String** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**proposals** | [**List&lt;AgentProposal&gt;**](AgentProposal.md) | Only on &#x60;GET /agent-runs/{runUuid}&#x60;. |  [optional] |



## Enum: TriggerEnum

| Name | Value |
|---- | -----|
| SCHEDULE | &quot;schedule&quot; |
| MANUAL | &quot;manual&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| QUEUED | &quot;queued&quot; |
| RUNNING | &quot;running&quot; |
| SUCCEEDED | &quot;succeeded&quot; |
| FAILED | &quot;failed&quot; |
| SKIPPED | &quot;skipped&quot; |



