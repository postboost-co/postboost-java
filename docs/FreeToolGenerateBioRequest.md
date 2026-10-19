

# FreeToolGenerateBioRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | What you or your brand do, and for whom. |  |
|**tone** | [**ToneEnum**](#ToneEnum) |  |  [optional] |
|**emoji** | **Boolean** | Use one or two fitting emoji. |  [optional] |
|**cta** | **Boolean** | End with a short call to action, such as the link in bio. |  [optional] |
|**network** | [**NetworkEnum**](#NetworkEnum) | The network the bio is written for (Instagram for now). |  [optional] |
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



