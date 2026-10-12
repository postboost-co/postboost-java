

# RepurposeResult


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**source** | [**RepurposeResultSource**](RepurposeResultSource.md) |  |  |
|**captions** | [**List&lt;BlogToSocialCaption&gt;**](BlogToSocialCaption.md) |  |  |
|**slides** | [**List&lt;RepurposeSlide&gt;**](RepurposeSlide.md) | Carousel slides in order (hook first, call to action last). Empty without a carousel. |  |
|**media** | [**RepurposeResultMedia**](RepurposeResultMedia.md) |  |  [optional] |
|**postUuid** | **UUID** | The draft post; null when &#x60;create_post&#x60; was false. |  |
|**creditsUsed** | **Integer** |  |  |
|**creditsRemaining** | **Integer** | Null for unlimited plans. |  |
|**warnings** | **List&lt;String&gt;** | Parts that were skipped (for example a network that gets no carousel). |  |



