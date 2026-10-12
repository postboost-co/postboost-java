

# BlogToSocialInput

At least one of `url` or (`title` + `excerpt`) must be provided. If both are given, direct values take priority over the scraped URL content. 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **URI** | Blog post URL to scrape. Required if &#x60;title&#x60; and &#x60;excerpt&#x60; are not provided. |  [optional] |
|**title** | **String** | Blog post title. Required if &#x60;url&#x60; is not provided. |  [optional] |
|**excerpt** | **String** | Blog post summary or excerpt. Required if &#x60;url&#x60; is not provided. |  [optional] |
|**imageUrl** | **URI** | Featured image URL for the blog post. When &#x60;create_post&#x60; is &#x60;true&#x60;, the image is imported into the workspace media library and attached to the draft post. If omitted in URL mode, the scraper attempts to extract the &#x60;og:image&#x60; meta tag.  |  [optional] |
|**platforms** | [**List&lt;PlatformsEnum&gt;**](#List&lt;PlatformsEnum&gt;) | Target social media platforms. Only connected accounts matching these platforms are used. If omitted, all connected accounts in the workspace are targeted.  |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** | Specific account IDs to generate captions for. Takes precedence over &#x60;platforms&#x60; when both are provided.  |  [optional] |
|**tone** | [**ToneEnum**](#ToneEnum) | Writing tone for all generated captions. |  [optional] |
|**contentLength** | [**ContentLengthEnum**](#ContentLengthEnum) | Desired length of the generated captions. |  [optional] |
|**hashtags** | [**HashtagsEnum**](#HashtagsEnum) | Hashtag quantity: none (0), few (1-3), some (3-5), many (5+). |  [optional] |
|**cta** | [**CtaEnum**](#CtaEnum) | Call-to-action type appended to each caption. |  [optional] |
|**language** | **String** | Output language as an ISO 639-1 code (e.g. &#x60;en&#x60;, &#x60;de&#x60;, &#x60;fr&#x60;). Use &#x60;auto&#x60; to match the blog post&#39;s language automatically.  |  [optional] |
|**customInstructions** | **String** | Additional instructions appended to the AI prompt (e.g. \&quot;always mention our free tier\&quot;). |  [optional] |
|**createPost** | **Boolean** | When &#x60;true&#x60;, creates a draft post in the workspace with per-account caption versions. If an image is available, it is imported and attached to the post.  |  [optional] |
|**useBrandVoice** | **Boolean** | Apply the workspace brand voice (see &#x60;GET brand-voice&#x60;) to the captions. An explicit &#x60;tone&#x60; is kept, but the brand voice wins on vocabulary, words to avoid and calls to action.  |  [optional] |



## Enum: List&lt;PlatformsEnum&gt;

| Name | Value |
|---- | -----|
| TWITTER | &quot;twitter&quot; |
| FACEBOOK_PAGE | &quot;facebook_page&quot; |
| INSTAGRAM | &quot;instagram&quot; |
| THREADS | &quot;threads&quot; |
| MASTODON | &quot;mastodon&quot; |
| YOUTUBE | &quot;youtube&quot; |
| GBP | &quot;gbp&quot; |
| PINTEREST | &quot;pinterest&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| LINKEDIN_PAGE | &quot;linkedin_page&quot; |
| TIKTOK | &quot;tiktok&quot; |
| BLUESKY | &quot;bluesky&quot; |



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



