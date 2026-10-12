

# RecyclingRule


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** |  |  |
|**type** | [**TypeEnum**](#TypeEnum) |  |  |
|**postUuid** | **String** |  |  |
|**tagUuid** | **String** |  |  |
|**accountIds** | **List&lt;Integer&gt;** |  |  |
|**intervalDays** | **Integer** |  |  |
|**maxRuns** | **Integer** |  |  |
|**runsDone** | **Integer** | Copies created so far. |  |
|**placement** | [**PlacementEnum**](#PlacementEnum) |  |  |
|**active** | **Boolean** |  |  |
|**nextRunAt** | **OffsetDateTime** |  |  |
|**lastRunAt** | **OffsetDateTime** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| POST | &quot;post&quot; |
| TAG_POOL | &quot;tag_pool&quot; |



## Enum: PlacementEnum

| Name | Value |
|---- | -----|
| QUEUE | &quot;queue&quot; |
| SAME_TIME | &quot;same_time&quot; |
| DRAFT | &quot;draft&quot; |



