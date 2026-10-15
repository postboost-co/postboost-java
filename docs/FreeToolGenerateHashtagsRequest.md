

# FreeToolGenerateHashtagsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**topic** | **String** | What the post is about. |  |
|**niche** | [**NicheEnum**](#NicheEnum) | Optional niche from the hashtag generator page. |  [optional] |
|**network** | [**NetworkEnum**](#NetworkEnum) | The network the text is written for. |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |



## Enum: NicheEnum

| Name | Value |
|---- | -----|
| FITNESS | &quot;Fitness&quot; |
| FOOD_AND_RESTAURANTS | &quot;Food and restaurants&quot; |
| TRAVEL | &quot;Travel&quot; |
| FASHION | &quot;Fashion&quot; |
| BEAUTY_AND_SKINCARE | &quot;Beauty and skincare&quot; |
| SMALL_BUSINESS | &quot;Small business&quot; |
| REAL_ESTATE | &quot;Real estate&quot; |
| PHOTOGRAPHY | &quot;Photography&quot; |
| MARKETING_AND_SOCIAL_MEDIA | &quot;Marketing and social media&quot; |
| TECH_AND_SAA_S | &quot;Tech and SaaS&quot; |
| PETS | &quot;Pets&quot; |
| EDUCATION_AND_COACHING | &quot;Education and coaching&quot; |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| FACEBOOK | &quot;facebook&quot; |



