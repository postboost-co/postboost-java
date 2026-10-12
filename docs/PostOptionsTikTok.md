

# PostOptionsTikTok

TikTok options. Every field is a map of `account-<account id>` to a value, so one post can carry different settings for several TikTok accounts. 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**privacyLevel** | [**Map&lt;String, InnerEnum&gt;**](#Map&lt;String, InnerEnum&gt;) |  |  [optional] |
|**isAigc** | **Map&lt;String, Boolean&gt;** | TikTok&#39;s \&quot;AI-generated content\&quot; label. |  [optional] |
|**allowComments** | **Map&lt;String, Boolean&gt;** |  |  [optional] |
|**allowDuet** | **Map&lt;String, Boolean&gt;** |  |  [optional] |
|**allowStitch** | **Map&lt;String, Boolean&gt;** |  |  [optional] |
|**autoAddMusic** | **Map&lt;String, Boolean&gt;** |  |  [optional] |
|**contentDisclosure** | **Map&lt;String, Boolean&gt;** | Discloses branded or promotional content; then set &#x60;brand_organic_toggle&#x60; and/or &#x60;brand_content_toggle&#x60;. |  [optional] |
|**brandOrganicToggle** | **Map&lt;String, Boolean&gt;** |  |  [optional] |
|**brandContentToggle** | **Map&lt;String, Boolean&gt;** |  |  [optional] |



## Enum: Map&lt;String, InnerEnum&gt;

| Name | Value |
|---- | -----|
| PUBLIC_TO_EVERYONE | &quot;PUBLIC_TO_EVERYONE&quot; |
| MUTUAL_FOLLOW_FRIENDS | &quot;MUTUAL_FOLLOW_FRIENDS&quot; |
| SELF_ONLY | &quot;SELF_ONLY&quot; |
| FOLLOWER_OF_CREATOR | &quot;FOLLOWER_OF_CREATOR&quot; |
| EMPTY | &quot;&quot; |



