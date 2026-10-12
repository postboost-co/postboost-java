

# RecyclingRuleUpdate


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**intervalDays** | **Integer** |  |  [optional] |
|**maxRuns** | **Integer** |  |  [optional] |
|**placement** | [**PlacementEnum**](#PlacementEnum) |  |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** |  |  [optional] |
|**startAt** | **OffsetDateTime** | Next run. |  [optional] |
|**active** | **Boolean** |  |  [optional] |



## Enum: PlacementEnum

| Name | Value |
|---- | -----|
| QUEUE | &quot;queue&quot; |
| SAME_TIME | &quot;same_time&quot; |
| DRAFT | &quot;draft&quot; |



