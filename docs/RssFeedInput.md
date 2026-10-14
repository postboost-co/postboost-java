

# RssFeedInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **URI** | Public http(s) URL of an RSS 2.0 or Atom feed. |  |
|**name** | **String** |  |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** |  |  |
|**mode** | [**ModeEnum**](#ModeEnum) |  |  [optional] |
|**template** | **String** | Post text. Placeholders: &#x60;{title}&#x60;, &#x60;{link}&#x60;, &#x60;{summary}&#x60; (up to 280 characters). Default &#x60;{title}&#x60; + blank line + &#x60;{link}&#x60;. |  [optional] |
|**maxItemsPerRun** | **Integer** |  |  [optional] |
|**active** | **Boolean** |  |  [optional] |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| QUEUE | &quot;queue&quot; |
| NEEDS_APPROVAL | &quot;needs_approval&quot; |



