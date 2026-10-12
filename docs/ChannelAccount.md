

# ChannelAccount

A connected Telegram, Discord or Slack channel. Same fields as `Account`.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**uuid** | **UUID** |  |  |
|**name** | **String** |  |  |
|**username** | **String** | Telegram public channel username; null for private channels, Discord and Slack. |  [optional] |
|**image** | **String** |  |  [optional] |
|**provider** | [**ProviderEnum**](#ProviderEnum) |  |  |
|**data** | **Object** | Provider metadata (Telegram &#x60;chat_id&#x60;, Discord &#x60;channel_id&#x60;/&#x60;guild_id&#x60;, Slack &#x60;team_id&#x60;). |  |
|**authorized** | **Boolean** |  |  |
|**profileUrl** | **String** |  |  [optional] |
|**createdAt** | **String** |  |  |



## Enum: ProviderEnum

| Name | Value |
|---- | -----|
| TELEGRAM | &quot;telegram&quot; |
| DISCORD | &quot;discord&quot; |
| SLACK | &quot;slack&quot; |



