

# RecyclingRuleInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**intervalDays** | **Integer** | Days between copies. |  |
|**maxRuns** | **Integer** | Copies to create before the rule stops; null &#x3D; no limit. |  [optional] |
|**placement** | [**PlacementEnum**](#PlacementEnum) | &#x60;queue&#x60;: each account&#39;s next free queue slot (skipped when the queue is full for 14 days). &#x60;same_time&#x60;: the source post&#39;s time of day. &#x60;draft&#x60;: a draft only. |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** | Accounts for the copies; default the source post&#39;s accounts. For a tag pool, limits each picked post&#39;s accounts. |  [optional] |
|**startAt** | **OffsetDateTime** | First run; default one interval from now. |  [optional] |
|**active** | **Boolean** |  |  [optional] |
|**type** | [**TypeEnum**](#TypeEnum) | Defaults to &#x60;post&#x60; when &#x60;post_uuid&#x60; is sent, else &#x60;tag_pool&#x60;. |  [optional] |
|**postUuid** | **UUID** | The post to recycle (type &#x60;post&#x60;). |  [optional] |
|**tagUuid** | **UUID** | The tag whose published posts are recycled, least recently recycled first (type &#x60;tag_pool&#x60;). |  [optional] |



## Enum: PlacementEnum

| Name | Value |
|---- | -----|
| QUEUE | &quot;queue&quot; |
| SAME_TIME | &quot;same_time&quot; |
| DRAFT | &quot;draft&quot; |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| POST | &quot;post&quot; |
| TAG_POOL | &quot;tag_pool&quot; |



