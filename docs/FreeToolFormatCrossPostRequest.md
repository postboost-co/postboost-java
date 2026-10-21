

# FreeToolFormatCrossPostRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | The post text, up to 10,000 characters. |  [optional] |
|**networks** | [**Set&lt;NetworksEnum&gt;**](#Set&lt;NetworksEnum&gt;) | The networks to format for, in the order the result lists them. |  [optional] |
|**numbering** | **Boolean** | End each post of a thread with \&quot; k/n\&quot;. |  [optional] |



## Enum: Set&lt;NetworksEnum&gt;

| Name | Value |
|---- | -----|
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| LINKEDIN | &quot;linkedin&quot; |



