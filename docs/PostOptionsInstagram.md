

# PostOptionsInstagram

Instagram options (`instagram` for accounts connected through Facebook, `instagram_standalone` for Instagram Login).

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) |  |  [optional] |
|**collaborators** | **List&lt;String&gt;** | Usernames invited as collaborators (not for stories). |  [optional] |
|**aiGenerated** | **Boolean** | Instagram&#39;s \&quot;AI info\&quot; label on the post (on the carousel itself for carousels; not for stories). Set by &#x60;ai_generated&#x60;. |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| POST | &quot;post&quot; |
| REEL | &quot;reel&quot; |
| STORY | &quot;story&quot; |



