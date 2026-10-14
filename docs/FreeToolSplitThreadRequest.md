

# FreeToolSplitThreadRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | The long text, up to 10,000 characters. A line with only --- forces a new post. |  [optional] |
|**network** | [**NetworkEnum**](#NetworkEnum) |  |  [optional] |
|**numbering** | **Boolean** | End each post with \&quot; k/n\&quot;. |  [optional] |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |



