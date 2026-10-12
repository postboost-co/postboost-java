

# WebhookSubscriptionInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**callbackUrl** | **URI** | Public &#x60;https://&#x60; URL that receives the deliveries. |  |
|**events** | **List&lt;WebhookEventName&gt;** |  |  |
|**name** | **String** | Label shown in Settings → Webhooks. Defaults to \&quot;&lt;Source&gt; trigger\&quot;. |  [optional] |
|**source** | [**SourceEnum**](#SourceEnum) | The tool creating the subscription. |  [optional] |



## Enum: SourceEnum

| Name | Value |
|---- | -----|
| N8N | &quot;n8n&quot; |
| ZAPIER | &quot;zapier&quot; |
| MAKE | &quot;make&quot; |
| OTHER | &quot;other&quot; |



