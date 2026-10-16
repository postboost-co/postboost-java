

# FreeToolGenerateSocialPostsFromBlogRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **URI** | Public http(s) address of the blog post. Give &#x60;url&#x60; or &#x60;text&#x60;. |  [optional] |
|**text** | **String** | The blog post itself, instead of &#x60;url&#x60;. |  [optional] |
|**platforms** | [**Set&lt;PlatformsEnum&gt;**](#Set&lt;PlatformsEnum&gt;) | Networks to write for, at most 4 per call (one AI credit each). |  |
|**tone** | [**ToneEnum**](#ToneEnum) |  |  [optional] |
|**length** | [**LengthEnum**](#LengthEnum) |  |  [optional] |
|**hashtags** | [**HashtagsEnum**](#HashtagsEnum) | How many hashtags to include. |  [optional] |
|**cta** | [**CtaEnum**](#CtaEnum) | Call to action to end with. |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |



## Enum: Set&lt;PlatformsEnum&gt;

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



## Enum: ToneEnum

| Name | Value |
|---- | -----|
| CASUAL | &quot;casual&quot; |
| PROFESSIONAL | &quot;professional&quot; |
| HUMOROUS | &quot;humorous&quot; |
| FORMAL | &quot;formal&quot; |
| FRIENDLY | &quot;friendly&quot; |
| CONVERSATIONAL | &quot;conversational&quot; |
| INFORMATIVE | &quot;informative&quot; |
| INSPIRATIONAL | &quot;inspirational&quot; |
| PLAYFUL | &quot;playful&quot; |
| AUTHORITATIVE | &quot;authoritative&quot; |
| EMPATHETIC | &quot;empathetic&quot; |
| PERSUASIVE | &quot;persuasive&quot; |
| SARCASTIC | &quot;sarcastic&quot; |
| TRENDY | &quot;trendy&quot; |
| NEUTRAL | &quot;neutral&quot; |
| EXCITED | &quot;excited&quot; |
| CALM | &quot;calm&quot; |
| BOLD | &quot;bold&quot; |
| ENERGETIC | &quot;energetic&quot; |
| ENCOURAGING | &quot;encouraging&quot; |



## Enum: LengthEnum

| Name | Value |
|---- | -----|
| SHORT | &quot;short&quot; |
| MEDIUM | &quot;medium&quot; |
| LONG | &quot;long&quot; |



## Enum: HashtagsEnum

| Name | Value |
|---- | -----|
| NO | &quot;no&quot; |
| FEW | &quot;few&quot; |
| SOME | &quot;some&quot; |
| MANY | &quot;many&quot; |



## Enum: CtaEnum

| Name | Value |
|---- | -----|
| NO | &quot;no&quot; |
| QUESTION | &quot;question&quot; |
| LINK | &quot;link&quot; |
| SUBSCRIBE | &quot;subscribe&quot; |
| FOLLOW | &quot;follow&quot; |
| SHARE | &quot;share&quot; |
| LEARN_MORE | &quot;learn more&quot; |
| SIGNUP | &quot;signup&quot; |
| BUY | &quot;buy&quot; |
| DOWNLOAD | &quot;download&quot; |



