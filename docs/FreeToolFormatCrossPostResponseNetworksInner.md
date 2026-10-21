

# FreeToolFormatCrossPostResponseNetworksInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**key** | [**KeyEnum**](#KeyEnum) |  |  [optional] |
|**label** | **String** |  |  [optional] |
|**limit** | **Integer** |  |  [optional] |
|**count** | **Integer** | Length as the network counts it. |  [optional] |
|**fits** | **Boolean** |  |  [optional] |
|**overBy** | **Integer** | Characters over the limit; 0 when it fits. |  [optional] |
|**links** | **Integer** | Unique http(s) links in the text (trailing punctuation trimmed), as Threads counts them. |  [optional] |
|**warnings** | [**List&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: threads_too_many_links, cut_by_fold, mentions_not_portable. |  [optional] |
|**thread** | [**List&lt;FreeToolFormatCrossPostResponseNetworksInnerThreadInner&gt;**](FreeToolFormatCrossPostResponseNetworksInnerThreadInner.md) | The thread for a text that does not fit (X, Threads, Bluesky, Mastodon); null when it fits or on LinkedIn. |  [optional] |



## Enum: KeyEnum

| Name | Value |
|---- | -----|
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| LINKEDIN | &quot;linkedin&quot; |



