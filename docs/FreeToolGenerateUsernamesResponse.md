

# FreeToolGenerateUsernamesResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**network** | [**NetworkEnum**](#NetworkEnum) |  |  [optional] |
|**style** | [**StyleEnum**](#StyleEnum) |  |  [optional] |
|**seed** | **Integer** |  |  [optional] |
|**usernames** | [**List&lt;FreeToolGenerateUsernamesResponseUsernamesInner&gt;**](FreeToolGenerateUsernamesResponseUsernamesInner.md) | Up to 30 names, each valid for the network. Not checked for availability: open the profile URL to see whether a name is taken. |  [optional] |
|**rules** | [**FreeToolGenerateUsernamesResponseRules**](FreeToolGenerateUsernamesResponseRules.md) |  |  [optional] |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| X | &quot;x&quot; |
| YOUTUBE | &quot;youtube&quot; |
| THREADS | &quot;threads&quot; |



## Enum: StyleEnum

| Name | Value |
|---- | -----|
| CLEAN | &quot;clean&quot; |
| CREATIVE | &quot;creative&quot; |
| BUSINESS | &quot;business&quot; |
| GAMING | &quot;gaming&quot; |



