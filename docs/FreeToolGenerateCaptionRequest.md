

# FreeToolGenerateCaptionRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | What the post is about. |  |
|**tone** | [**ToneEnum**](#ToneEnum) |  |  [optional] |
|**length** | [**LengthEnum**](#LengthEnum) | short: 10-20 words, medium: 25-40, long: 45-60. |  [optional] |
|**emoji** | **Boolean** | Use a few fitting emoji. |  [optional] |
|**hashtags** | **Boolean** | End each caption with 3-5 relevant hashtags. |  [optional] |
|**network** | [**NetworkEnum**](#NetworkEnum) | The network the text is written for. |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |
|**format** | [**FormatEnum**](#FormatEnum) | caption: short captions (default). post: long-form posts of 300-600, 600-1,300 or 1,300-2,000 characters by &#x60;length&#x60;, with at most 3 hashtags; network linkedin only. |  [optional] |



## Enum: ToneEnum

| Name | Value |
|---- | -----|
| FRIENDLY | &quot;friendly&quot; |
| PROFESSIONAL | &quot;professional&quot; |
| PLAYFUL | &quot;playful&quot; |
| INSPIRATIONAL | &quot;inspirational&quot; |
| BOLD | &quot;bold&quot; |



## Enum: LengthEnum

| Name | Value |
|---- | -----|
| SHORT | &quot;short&quot; |
| MEDIUM | &quot;medium&quot; |
| LONG | &quot;long&quot; |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| FACEBOOK | &quot;facebook&quot; |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| CAPTION | &quot;caption&quot; |
| POST | &quot;post&quot; |



