

# FreeToolGenerateHashtagsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**topic** | **String** | What the post is about. |  |
|**niche** | **String** | Optional niche, e.g. \&quot;fitness\&quot; or \&quot;real estate\&quot;. |  [optional] |
|**network** | [**NetworkEnum**](#NetworkEnum) | The network the text is written for. |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| FACEBOOK | &quot;facebook&quot; |



