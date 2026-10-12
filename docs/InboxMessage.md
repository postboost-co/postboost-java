

# InboxMessage


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Message UUID. |  |
|**direction** | [**DirectionEnum**](#DirectionEnum) |  |  |
|**body** | **String** |  |  |
|**author** | [**InboxMessageAuthor**](InboxMessageAuthor.md) |  |  [optional] |
|**sentiment** | [**SentimentEnum**](#SentimentEnum) |  |  [optional] |
|**aiLabel** | [**AiLabelEnum**](#AiLabelEnum) |  |  [optional] |
|**isSpam** | **Boolean** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: DirectionEnum

| Name | Value |
|---- | -----|
| INBOUND | &quot;inbound&quot; |
| OUTBOUND | &quot;outbound&quot; |



## Enum: SentimentEnum

| Name | Value |
|---- | -----|
| NEGATIVE | &quot;negative&quot; |
| NEUTRAL | &quot;neutral&quot; |
| POSITIVE | &quot;positive&quot; |



## Enum: AiLabelEnum

| Name | Value |
|---- | -----|
| QUESTION | &quot;question&quot; |
| COMPLAINT | &quot;complaint&quot; |
| PRAISE | &quot;praise&quot; |
| LEAD | &quot;lead&quot; |
| OTHER | &quot;other&quot; |



