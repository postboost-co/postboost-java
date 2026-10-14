

# PostWarning

A non-blocking warning on a successful create or update: the post was saved, but something will not behave as you may expect. Log the `code`. - `ai_media_without_disclosure`: the post uses media from the AI image endpoints but   `ai_generated` is `false`, so no network AI label is applied. - `meta_first_comment_unavailable`: a Facebook Page or Instagram first comment cannot   be published yet (Meta is reviewing our access); the post itself publishes. 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**code** | [**CodeEnum**](#CodeEnum) |  |  |
|**accountId** | **Integer** | The account the warning is about; null when it is about the whole post. |  |
|**message** | **String** |  |  |



## Enum: CodeEnum

| Name | Value |
|---- | -----|
| AI_MEDIA_WITHOUT_DISCLOSURE | &quot;ai_media_without_disclosure&quot; |
| META_FIRST_COMMENT_UNAVAILABLE | &quot;meta_first_comment_unavailable&quot; |



