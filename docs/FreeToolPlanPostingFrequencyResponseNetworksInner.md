

# FreeToolPlanPostingFrequencyResponseNetworksInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**network** | [**NetworkEnum**](#NetworkEnum) |  |  [optional] |
|**label** | **String** |  |  [optional] |
|**recommendedPerWeek** | [**FreeToolPlanPostingFrequencyResponseNetworksInnerRecommendedPerWeek**](FreeToolPlanPostingFrequencyResponseNetworksInnerRecommendedPerWeek.md) |  |  [optional] |
|**recommendedLabel** | **String** | The range as text, e.g. \&quot;3-5 per week\&quot; or \&quot;1+ per week\&quot;. |  [optional] |
|**allocatedPerWeek** | **Integer** | Your posts for this network: capacity split in proportion to the range midpoints (the minimum for an open-ended range). |  [optional] |
|**fit** | [**FitEnum**](#FitEnum) | Where the allocation sits against the recommended range. |  [optional] |
|**sourceType** | [**SourceTypeEnum**](#SourceTypeEnum) | measured &#x3D; a study of real posts; vendor &#x3D; a software vendor&#39;s guidance; platform &#x3D; the network&#39;s own guidance. |  [optional] |
|**sources** | [**List&lt;FreeToolPlanPostingFrequencyResponseNetworksInnerSourcesInner&gt;**](FreeToolPlanPostingFrequencyResponseNetworksInnerSourcesInner.md) |  |  [optional] |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| FACEBOOK | &quot;facebook&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| TIKTOK | &quot;tiktok&quot; |
| YOUTUBE | &quot;youtube&quot; |
| PINTEREST | &quot;pinterest&quot; |
| THREADS | &quot;threads&quot; |
| GOOGLE_BUSINESS_PROFILE | &quot;google_business_profile&quot; |



## Enum: FitEnum

| Name | Value |
|---- | -----|
| BELOW | &quot;below&quot; |
| WITHIN | &quot;within&quot; |
| ABOVE | &quot;above&quot; |



## Enum: SourceTypeEnum

| Name | Value |
|---- | -----|
| MEASURED | &quot;measured&quot; |
| VENDOR | &quot;vendor&quot; |
| PLATFORM | &quot;platform&quot; |



