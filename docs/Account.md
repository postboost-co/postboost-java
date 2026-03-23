

# Account


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**uuid** | **UUID** |  |  |
|**name** | **String** |  |  |
|**username** | **String** |  |  |
|**image** | **URI** |  |  [optional] |
|**provider** | [**ProviderEnum**](#ProviderEnum) |  |  |
|**data** | **Object** | Provider-specific metadata. |  |
|**authorized** | **Boolean** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



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



