

# Account


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**uuid** | **UUID** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**username** | **String** |  |  [optional] |
|**image** | **URI** |  |  [optional] |
|**provider** | [**ProviderEnum**](#ProviderEnum) |  |  [optional] |
|**data** | **Object** | Provider-specific metadata. |  [optional] |
|**authorized** | **Boolean** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: ProviderEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| PINTEREST | &quot;pinterest&quot; |
| TWITTER | &quot;twitter&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| FACEBOOK_PAGE | &quot;facebook_page&quot; |
| YOUTUBE | &quot;youtube&quot; |
| MASTODON | &quot;mastodon&quot; |



