

# AgentProposal


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** |  |  |
|**runUuid** | **UUID** |  |  [optional] |
|**postUuid** | **UUID** |  |  [optional] |
|**accountId** | **Integer** |  |  [optional] |
|**kind** | [**KindEnum**](#KindEnum) | &#x60;hold_post&#x60; moves the post back to draft; &#x60;edit_caption&#x60; replaces one caption. |  |
|**severity** | [**SeverityEnum**](#SeverityEnum) |  |  |
|**reason** | **String** |  |  |
|**payload** | **Map&lt;String, Object&gt;** | The proposed change. &#x60;hold_post&#x60;: &#x60;reasons[]&#x60; (&#x60;code&#x60;, &#x60;account_id&#x60;, &#x60;message&#x60;, &#x60;severity&#x60;) and &#x60;scheduled_at&#x60;. &#x60;edit_caption&#x60;: &#x60;version_account_id&#x60; (0 &#x3D; original), &#x60;item_index&#x60;, &#x60;before&#x60;, &#x60;after&#x60;. Both carry &#x60;post_updated_at&#x60;.  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**decidedAt** | **OffsetDateTime** |  |  [optional] |
|**appliedAt** | **OffsetDateTime** |  |  [optional] |
|**note** | **String** |  |  [optional] |
|**error** | **String** | Why a proposal went stale or failed. |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: KindEnum

| Name | Value |
|---- | -----|
| HOLD_POST | &quot;hold_post&quot; |
| EDIT_CAPTION | &quot;edit_caption&quot; |



## Enum: SeverityEnum

| Name | Value |
|---- | -----|
| INFO | &quot;info&quot; |
| WARNING | &quot;warning&quot; |
| CRITICAL | &quot;critical&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| APPLIED | &quot;applied&quot; |
| REJECTED | &quot;rejected&quot; |
| STALE | &quot;stale&quot; |
| FAILED | &quot;failed&quot; |
| EXPIRED | &quot;expired&quot; |



