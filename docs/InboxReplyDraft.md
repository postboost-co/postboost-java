

# InboxReplyDraft


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Draft UUID. |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**body** | **String** |  |  |
|**source** | [**SourceEnum**](#SourceEnum) |  |  |
|**conversationId** | **String** |  |  [optional] |
|**provider** | **String** |  |  [optional] |
|**inReplyTo** | **Object** | The incoming message this replies to (same shape as &#x60;InboxMessage&#x60;). |  [optional] |
|**createdBy** | **String** | Name of the user whose API key wrote the draft. |  [optional] |
|**reviewedBy** | **String** |  |  [optional] |
|**reviewedAt** | **OffsetDateTime** |  |  [optional] |
|**sentMessageId** | **String** | The sent reply&#39;s message UUID, once sent. |  [optional] |
|**error** | **String** | Why sending failed. |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| APPROVED | &quot;approved&quot; |
| REJECTED | &quot;rejected&quot; |
| SENT | &quot;sent&quot; |
| FAILED | &quot;failed&quot; |



## Enum: SourceEnum

| Name | Value |
|---- | -----|
| API | &quot;api&quot; |
| MCP | &quot;mcp&quot; |
| WEB | &quot;web&quot; |



