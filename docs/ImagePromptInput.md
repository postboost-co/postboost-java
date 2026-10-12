

# ImagePromptInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**caption** | **String** |  |  |
|**platform** | **String** |  |  |
|**template** | [**TemplateEnum**](#TemplateEnum) |  |  [optional] |
|**style** | **String** |  |  [optional] |
|**brandVoice** | **String** | Free-text tone for the image. When sent, it replaces the stored workspace brand voice for this call. |  [optional] |
|**useBrandVoice** | **Boolean** | When &#x60;brand_voice&#x60; is not sent, derive the image tone from the workspace brand voice. Ignored in developer mode (&#x60;prompt&#x60;). |  [optional] |
|**customInstructions** | **String** |  |  [optional] |



## Enum: TemplateEnum

| Name | Value |
|---- | -----|
| BLOG_COVER | &quot;blog_cover&quot; |
| QUOTE_CARD | &quot;quote_card&quot; |
| STAT_CARD | &quot;stat_card&quot; |
| FEATURE_ANNOUNCEMENT | &quot;feature_announcement&quot; |
| PRODUCT_HIGHLIGHT | &quot;product_highlight&quot; |
| EVENT_PROMO | &quot;event_promo&quot; |
| CAROUSEL_SLIDE | &quot;carousel_slide&quot; |
| AD_CREATIVE | &quot;ad_creative&quot; |



