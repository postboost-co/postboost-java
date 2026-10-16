

# FreeToolGenerateHooksRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**topic** | **String** | What the post is about. |  |
|**tone** | [**ToneEnum**](#ToneEnum) | Tone of the hooks, as on the caption generator. |  [optional] |
|**count** | **Integer** | How many hooks to write. |  [optional] |
|**network** | [**NetworkEnum**](#NetworkEnum) | The network the text is written for. |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |



## Enum: ToneEnum

| Name | Value |
|---- | -----|
| FRIENDLY | &quot;friendly&quot; |
| PROFESSIONAL | &quot;professional&quot; |
| PLAYFUL | &quot;playful&quot; |
| INSPIRATIONAL | &quot;inspirational&quot; |
| BOLD | &quot;bold&quot; |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| FACEBOOK | &quot;facebook&quot; |



