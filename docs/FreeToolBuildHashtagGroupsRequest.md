

# FreeToolBuildHashtagGroupsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** | Hashtags or words, separated by spaces, commas or new lines. A missing # is added. |  |
|**network** | [**NetworkEnum**](#NetworkEnum) | Network whose hashtag cap applies. |  [optional] |
|**groupSize** | **Integer** | Hashtags per group. Default: the network&#39;s cap, or 5 when it has no hard cap. |  [optional] |
|**_case** | [**CaseEnum**](#CaseEnum) | keep the first spelling of each hashtag, or lower-case all of them. |  [optional] |
|**format** | [**FormatEnum**](#FormatEnum) | inline: one line of tags. first_comment: five \&quot;.\&quot; lines, then the tags. |  [optional] |



## Enum: NetworkEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| FACEBOOK | &quot;facebook&quot; |
| TIKTOK | &quot;tiktok&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| YOUTUBE | &quot;youtube&quot; |



## Enum: CaseEnum

| Name | Value |
|---- | -----|
| KEEP | &quot;keep&quot; |
| LOWER | &quot;lower&quot; |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| INLINE | &quot;inline&quot; |
| FIRST_COMMENT | &quot;first_comment&quot; |



