

# FreeToolPickSocialMediaToolResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**needs** | [**List&lt;NeedsEnum&gt;**](#List&lt;NeedsEnum&gt;) | The needs matched, deduplicated, in a fixed order. |  [optional] |
|**results** | [**List&lt;FreeToolPickSocialMediaToolResponseResultsInner&gt;**](FreeToolPickSocialMediaToolResponseResultsInner.md) | Every tool compared, PostBoost included: by score (highest first), then name. |  [optional] |
|**checkedAt** | **LocalDate** | Date of the comparison data snapshot. |  [optional] |
|**checkedLabel** | **String** | The snapshot month, as shown on the page. |  [optional] |



## Enum: List&lt;NeedsEnum&gt;

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



