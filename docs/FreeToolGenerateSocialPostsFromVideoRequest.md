

# FreeToolGenerateSocialPostsFromVideoRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | The captions of your video: an .srt, .vtt or .sbv file&#39;s text, or the text of YouTube&#39;s \&quot;Show transcript\&quot; panel. Timestamps, cue numbers and sound tags like [Music] are removed; 100 to 24,000 characters must remain. |  |
|**videoUrl** | **String** | The video&#39;s YouTube link (watch, youtu.be, Shorts or live). Each output links it once, the X thread in its last post; without it the posts have no link. |  [optional] |
|**title** | **String** | The video&#39;s title, as context for the posts. |  [optional] |
|**outputs** | [**List&lt;OutputsEnum&gt;**](#List&lt;OutputsEnum&gt;) | What to write, 1 to 4 different keys. |  [optional] |
|**tone** | [**ToneEnum**](#ToneEnum) |  |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |



## Enum: List&lt;OutputsEnum&gt;

| Name | Value |
|---- | -----|
| X_THREAD | &quot;x_thread&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| INSTAGRAM | &quot;instagram&quot; |
| FACEBOOK | &quot;facebook&quot; |
| THREADS | &quot;threads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |



## Enum: ToneEnum

| Name | Value |
|---- | -----|
| FRIENDLY | &quot;friendly&quot; |
| PROFESSIONAL | &quot;professional&quot; |
| PLAYFUL | &quot;playful&quot; |
| INSPIRATIONAL | &quot;inspirational&quot; |
| BOLD | &quot;bold&quot; |



