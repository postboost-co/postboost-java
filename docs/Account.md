

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
|**profileUrl** | **URI** | Public URL of the account&#39;s profile on the network, when known. |  [optional] |
|**publishStatus** | [**PublishStatusEnum**](#PublishStatusEnum) | Only present when the account is embedded in a post. Publishing state of this account for the post. |  [optional] |
|**publishedParts** | **Integer** | Only present when the account is embedded in a post. How many parts (for example thread items or a first comment) are live on the network. |  [optional] |
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



## Enum: PublishStatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| PUBLISHING | &quot;publishing&quot; |
| PUBLISHED | &quot;published&quot; |
| FAILED | &quot;failed&quot; |



