

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
|**externalUrl** | **String** | Only present when the account is embedded in a post. URL of the published post on the network, null until it is live. |  [optional] |
|**errors** | [**List&lt;AccountErrorsInner&gt;**](AccountErrorsInner.md) | Only present when the account is embedded in a post. Why publishing to this account failed. A raw network error is stored as two entries: a readable line (&#x60;\&quot;&lt;Network&gt;: &lt;message&gt; (code &lt;code&gt;)\&quot;&#x60;) and an object &#x60;{platform, code, message, raw}&#x60; with the network&#39;s original response in &#x60;raw&#x60;. Other failures are a single readable string.  |  [optional] |
|**createdAt** | **String** | UTC, formatted &#x60;Y-m-d H:i:s&#x60;. |  |



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



