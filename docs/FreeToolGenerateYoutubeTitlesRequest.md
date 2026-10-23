

# FreeToolGenerateYoutubeTitlesRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | What the video is about. |  |
|**style** | [**StyleEnum**](#StyleEnum) | how-to (\&quot;How to ...\&quot;), listicle (\&quot;7 ways to ...\&quot;), question, story (first person) or news. |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |
|**transcript** | **String** | Optional: your video&#39;s captions (.srt, .vtt, .sbv or the Show transcript text) as context; timestamps are removed and the first 6,000 characters are used. |  [optional] |



## Enum: StyleEnum

| Name | Value |
|---- | -----|
| HOW_TO | &quot;how-to&quot; |
| LISTICLE | &quot;listicle&quot; |
| QUESTION | &quot;question&quot; |
| STORY | &quot;story&quot; |
| NEWS | &quot;news&quot; |



