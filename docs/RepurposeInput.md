

# RepurposeInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**sourceType** | [**SourceTypeEnum**](#SourceTypeEnum) |  |  |
|**url** | **URI** | Article URL (&#x60;url&#x60;) or YouTube video URL (&#x60;youtube&#x60;). For &#x60;text&#x60;, an optional link to mention. |  [optional] |
|**pdfUrl** | **URI** | Public URL of a PDF (&#x60;pdf&#x60;), at most 20 MB. |  [optional] |
|**title** | **String** | Required for &#x60;text&#x60;. For &#x60;youtube&#x60;, overrides the video title. |  [optional] |
|**text** | **String** | Required for &#x60;text&#x60;. Long sources are cut to about 12,000 characters. |  [optional] |
|**transcript** | **String** | Video transcript for &#x60;youtube&#x60;. |  [optional] |
|**platforms** | **List&lt;String&gt;** | Limit to connected accounts of these networks. Ignored when &#x60;account_ids&#x60; is set. |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** | Target accounts. Default is every connected account. |  [optional] |
|**tone** | [**ToneEnum**](#ToneEnum) |  |  [optional] |
|**contentLength** | [**ContentLengthEnum**](#ContentLengthEnum) |  |  [optional] |
|**hashtags** | [**HashtagsEnum**](#HashtagsEnum) |  |  [optional] |
|**cta** | [**CtaEnum**](#CtaEnum) |  |  [optional] |
|**language** | **String** |  |  [optional] |
|**customInstructions** | **String** |  |  [optional] |
|**carousel** | **Boolean** | Render carousel slides (one extra AI credit for the outline). |  [optional] |
|**slideCount** | **Integer** | Total slides including the hook and call-to-action slides. |  [optional] |
|**theme** | [**RepurposeInputTheme**](RepurposeInputTheme.md) |  |  [optional] |
|**createPost** | **Boolean** | Create the draft post. &#x60;false&#x60; returns captions and slides only. |  [optional] |
|**useBrandVoice** | **Boolean** |  |  [optional] |
|**async** | **Boolean** | Answer &#x60;202&#x60; with a run id right away instead of waiting up to 20 seconds for the result. |  [optional] |



## Enum: SourceTypeEnum

| Name | Value |
|---- | -----|
| URL | &quot;url&quot; |
| YOUTUBE | &quot;youtube&quot; |
| PDF | &quot;pdf&quot; |
| TEXT | &quot;text&quot; |



## Enum: ToneEnum

| Name | Value |
|---- | -----|
| NEUTRAL | &quot;neutral&quot; |
| FRIENDLY | &quot;friendly&quot; |
| FORMAL | &quot;formal&quot; |
| EDGY | &quot;edgy&quot; |
| ENGAGING | &quot;engaging&quot; |
| CASUAL | &quot;casual&quot; |
| PROFESSIONAL | &quot;professional&quot; |
| HUMOROUS | &quot;humorous&quot; |
| INSPIRATIONAL | &quot;inspirational&quot; |
| CONVERSATIONAL | &quot;conversational&quot; |



## Enum: ContentLengthEnum

| Name | Value |
|---- | -----|
| SHORT | &quot;short&quot; |
| MEDIUM | &quot;medium&quot; |
| LONG | &quot;long&quot; |



## Enum: HashtagsEnum

| Name | Value |
|---- | -----|
| NONE | &quot;none&quot; |
| FEW | &quot;few&quot; |
| SOME | &quot;some&quot; |
| MANY | &quot;many&quot; |



## Enum: CtaEnum

| Name | Value |
|---- | -----|
| NONE | &quot;none&quot; |
| QUESTION | &quot;question&quot; |
| LINK | &quot;link&quot; |
| SUBSCRIBE | &quot;subscribe&quot; |
| FOLLOW | &quot;follow&quot; |
| SHARE | &quot;share&quot; |
| LEARN_MORE | &quot;learn_more&quot; |
| SIGNUP | &quot;signup&quot; |
| BUY | &quot;buy&quot; |
| DOWNLOAD | &quot;download&quot; |



