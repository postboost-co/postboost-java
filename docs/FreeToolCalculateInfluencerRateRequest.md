

# FreeToolCalculateInfluencerRateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**network** | [**NetworkEnum**](#NetworkEnum) | LinkedIn is not offered: no primary source for its rates. |  |
|**followers** | **Integer** | Followers (subscribers on YouTube). Sets the tier. |  |
|**deliverable** | [**DeliverableEnum**](#DeliverableEnum) | Instagram: post (default), reel, carousel. TikTok: video. X and Facebook: post. YouTube: integration (default), dedicated, short. |  [optional] |
|**avgViews** | **Integer** | Expected views of the deliverable. Required on YouTube, which is priced per 1,000 views; with cpm_usd it gives your own CPM estimate on any network. |  [optional] |
|**cpmUsd** | **Integer** | Your own price per 1,000 views, in whole USD, for the CPM estimate. |  [optional] |
|**usageRightsMonths** | **Integer** | Months the brand may reuse the content. |  [optional] |
|**exclusivity** | **Boolean** | The creator agrees not to work with competitors for the campaign. |  [optional] |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| YOUTUBE | &quot;youtube&quot; |
| X | &quot;x&quot; |
| FACEBOOK | &quot;facebook&quot; |



## Enum: DeliverableEnum

| Name | Value |
|---- | -----|
| POST | &quot;post&quot; |
| REEL | &quot;reel&quot; |
| CAROUSEL | &quot;carousel&quot; |
| VIDEO | &quot;video&quot; |
| INTEGRATION | &quot;integration&quot; |
| DEDICATED | &quot;dedicated&quot; |
| SHORT | &quot;short&quot; |



