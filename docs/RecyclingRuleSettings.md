

# RecyclingRuleSettings


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**intervalDays** | **Integer** | Days between copies. |  |
|**maxRuns** | **Integer** | Copies to create before the rule stops; null &#x3D; no limit. |  [optional] |
|**placement** | [**PlacementEnum**](#PlacementEnum) | &#x60;queue&#x60;: each account&#39;s next free queue slot (skipped when the queue is full for 14 days). &#x60;same_time&#x60;: the source post&#39;s time of day. &#x60;draft&#x60;: a draft only. |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** | Accounts for the copies; default the source post&#39;s accounts. For a tag pool, limits each picked post&#39;s accounts. |  [optional] |
|**startAt** | **OffsetDateTime** | First run; default one interval from now. |  [optional] |
|**active** | **Boolean** |  |  [optional] |



## Enum: PlacementEnum

| Name | Value |
|---- | -----|
| QUEUE | &quot;queue&quot; |
| SAME_TIME | &quot;same_time&quot; |
| DRAFT | &quot;draft&quot; |



