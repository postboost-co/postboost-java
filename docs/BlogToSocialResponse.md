

# BlogToSocialResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**blogTitle** | **String** | The blog post title (scraped or provided directly). |  [optional] |
|**blogExcerpt** | **String** | A short excerpt from the blog post content. |  [optional] |
|**captions** | [**List&lt;BlogToSocialCaption&gt;**](BlogToSocialCaption.md) | Generated captions, one per target account. |  [optional] |
|**postUuid** | **UUID** | UUID of the created draft post. Only present when &#x60;create_post&#x60; was &#x60;true&#x60;. |  [optional] |
|**media** | [**BlogToSocialMedia**](BlogToSocialMedia.md) |  |  [optional] |
|**creditsUsed** | **Integer** | Number of AI credits consumed by this request (one per successful caption). |  [optional] |
|**creditsRemaining** | **Integer** | Remaining AI credits for the current billing period. &#x60;null&#x60; for unlimited plans. |  [optional] |



