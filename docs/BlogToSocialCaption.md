

# BlogToSocialCaption


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**accountId** | **Integer** | ID of the social account this caption was generated for. |  [optional] |
|**provider** | **String** | Social media platform identifier. |  [optional] |
|**content** | **String** | The generated caption text. &#x60;null&#x60; if generation failed for this account. |  [optional] |
|**characterCount** | **Integer** | Character count of the generated content. &#x60;null&#x60; if generation failed. |  [optional] |
|**characterLimit** | **Integer** | Maximum allowed character count for this platform. |  [optional] |
|**error** | **String** | Error message if caption generation failed for this account. &#x60;null&#x60; on success. |  [optional] |



