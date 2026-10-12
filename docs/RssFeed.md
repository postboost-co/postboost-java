

# RssFeed


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** |  |  |
|**url** | **String** |  |  |
|**name** | **String** |  |  |
|**accountIds** | **List&lt;Integer&gt;** |  |  |
|**mode** | [**ModeEnum**](#ModeEnum) |  |  |
|**template** | **String** |  |  |
|**maxItemsPerRun** | **Integer** |  |  |
|**active** | **Boolean** |  |  |
|**lastPolledAt** | **OffsetDateTime** |  |  |
|**lastError** | **String** | Error of the last check; after 5 failures in a row the feed is checked every 6 hours. |  |
|**createdAt** | **OffsetDateTime** |  |  |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| QUEUE | &quot;queue&quot; |



