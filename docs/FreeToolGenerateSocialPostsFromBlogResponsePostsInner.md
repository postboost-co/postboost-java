

# FreeToolGenerateSocialPostsFromBlogResponsePostsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**platform** | [**PlatformEnum**](#PlatformEnum) |  |  [optional] |
|**text** | **String** | The post, cut at a sentence end when the model ran over the limit. |  [optional] |
|**hashtags** | **List&lt;String&gt;** | Hashtags in the text, with #. |  [optional] |
|**characters** | **Integer** | Length as the network counts it (X weighs links as 23, YouTube counts bytes). |  [optional] |
|**limit** | **Integer** | The network&#39;s text limit. |  [optional] |



## Enum: PlatformEnum

| Name | Value |
|---- | -----|
| FACEBOOK | &quot;facebook&quot; |
| INSTAGRAM | &quot;instagram&quot; |
| X | &quot;x&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| PINTEREST | &quot;pinterest&quot; |
| YOUTUBE | &quot;youtube&quot; |
| TIKTOK | &quot;tiktok&quot; |
| MASTODON | &quot;mastodon&quot; |



