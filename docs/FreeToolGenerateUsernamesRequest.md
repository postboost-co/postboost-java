

# FreeToolGenerateUsernamesRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Your name, brand or a few keywords. Accents are dropped; only Latin letters and digits are used. |  |
|**network** | [**NetworkEnum**](#NetworkEnum) | Whose username rules apply (Threads uses your Instagram username). |  [optional] |
|**style** | [**StyleEnum**](#StyleEnum) | Which word list to mix in. |  [optional] |
|**numbers** | **Boolean** | Allow a number at the end of some names. |  [optional] |
|**seed** | **Integer** | The same input and seed give the same list; change it for more ideas. |  [optional] |



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



