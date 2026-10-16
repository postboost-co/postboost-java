

# FreeToolGetHookTemplatesResponseHooksInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | The hook, with &#x60;{topic}&#x60; filled in when a topic was given. |  [optional] |
|**template** | **String** | The template with its &#x60;{topic}&#x60; placeholder. |  [optional] |
|**category** | [**CategoryEnum**](#CategoryEnum) | Hook style. |  [optional] |
|**networks** | [**List&lt;NetworksEnum&gt;**](#List&lt;NetworksEnum&gt;) | Networks the hook suits. |  [optional] |



## Enum: CategoryEnum

| Name | Value |
|---- | -----|
| QUESTION | &quot;question&quot; |
| CONTRARIAN | &quot;contrarian&quot; |
| LIST | &quot;list&quot; |
| STORY | &quot;story&quot; |
| MISTAKE | &quot;mistake&quot; |
| HOW_TO | &quot;how-to&quot; |
| CURIOSITY | &quot;curiosity&quot; |
| SOCIAL_PROOF | &quot;social-proof&quot; |



## Enum: List&lt;NetworksEnum&gt;

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| TIKTOK | &quot;tiktok&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| FACEBOOK | &quot;facebook&quot; |



