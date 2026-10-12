

# ImageGenerateInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**caption** | **String** | Social media caption. Triggers standard mode. Takes priority over prompt. |  [optional] |
|**platform** | **String** | Required when caption is provided. |  [optional] |
|**template** | [**TemplateEnum**](#TemplateEnum) |  |  [optional] |
|**style** | **String** |  |  [optional] |
|**brandVoice** | **String** | Free-text tone for the image. When sent, it replaces the stored workspace brand voice for this call. |  [optional] |
|**useBrandVoice** | **Boolean** | When &#x60;brand_voice&#x60; is not sent, derive the image tone from the workspace brand voice. Ignored in developer mode (&#x60;prompt&#x60;). |  [optional] |
|**customInstructions** | **String** |  |  [optional] |
|**prompt** | **String** | Developer escape hatch. Bypasses internal prompt builder. Ignored if caption is present. |  [optional] |
|**aspectRatio** | [**AspectRatioEnum**](#AspectRatioEnum) |  |  [optional] |
|**count** | **Integer** |  |  [optional] |
|**quality** | [**QualityEnum**](#QualityEnum) |  |  [optional] |



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



## Enum: AspectRatioEnum

| Name | Value |
|---- | -----|
| _1_1 | &quot;1:1&quot; |
| _16_9 | &quot;16:9&quot; |
| _9_16 | &quot;9:16&quot; |
| _4_5 | &quot;4:5&quot; |



## Enum: QualityEnum

| Name | Value |
|---- | -----|
| STANDARD | &quot;standard&quot; |
| HD | &quot;hd&quot; |



