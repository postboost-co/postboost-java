

# FreeToolPickSocialMediaToolResponseResultsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**slug** | **String** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**score** | **Integer** | How many of your needs the tool meets. |  [optional] |
|**matched** | [**List&lt;MatchedEnum&gt;**](#List&lt;MatchedEnum&gt;) |  |  [optional] |
|**missing** | [**List&lt;MissingEnum&gt;**](#List&lt;MissingEnum&gt;) |  |  [optional] |
|**unknown** | [**List&lt;UnknownEnum&gt;**](#List&lt;UnknownEnum&gt;) | Needs the tool&#39;s public docs did not show either way (\&quot;not documented\&quot;). |  [optional] |
|**compareUrl** | **String** | Path of the full PostBoost comparison page; null for PostBoost. |  [optional] |
|**checkedAt** | **LocalDate** | When the tool&#39;s data was last checked. |  [optional] |
|**pickIf** | **String** | When this tool is the better choice; null for PostBoost. |  [optional] |
|**postboostIf** | **String** | When PostBoost is the better choice; null for PostBoost. |  [optional] |



## Enum: List&lt;MatchedEnum&gt;

| Name | Value |
|---- | -----|
| TEAM_DASHBOARD | &quot;team_dashboard&quot; |
| REST_OPENAPI | &quot;rest_openapi&quot; |
| SDKS | &quot;sdks&quot; |
| MCP | &quot;mcp&quot; |
| WEBHOOKS | &quot;webhooks&quot; |
| FREE_TIER | &quot;free_tier&quot; |
| ZAPIER | &quot;zapier&quot; |
| N8N | &quot;n8n&quot; |
| MAKE | &quot;make&quot; |



## Enum: List&lt;MissingEnum&gt;

| Name | Value |
|---- | -----|
| TEAM_DASHBOARD | &quot;team_dashboard&quot; |
| REST_OPENAPI | &quot;rest_openapi&quot; |
| SDKS | &quot;sdks&quot; |
| MCP | &quot;mcp&quot; |
| WEBHOOKS | &quot;webhooks&quot; |
| FREE_TIER | &quot;free_tier&quot; |
| ZAPIER | &quot;zapier&quot; |
| N8N | &quot;n8n&quot; |
| MAKE | &quot;make&quot; |



## Enum: List&lt;UnknownEnum&gt;

| Name | Value |
|---- | -----|
| TEAM_DASHBOARD | &quot;team_dashboard&quot; |
| REST_OPENAPI | &quot;rest_openapi&quot; |
| SDKS | &quot;sdks&quot; |
| MCP | &quot;mcp&quot; |
| WEBHOOKS | &quot;webhooks&quot; |
| FREE_TIER | &quot;free_tier&quot; |
| ZAPIER | &quot;zapier&quot; |
| N8N | &quot;n8n&quot; |
| MAKE | &quot;make&quot; |



