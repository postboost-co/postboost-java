

# ImageVariationsResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**images** | [**List&lt;Media&gt;**](Media.md) |  |  |
|**aspectRatio** | **String** |  |  |
|**quality** | **String** |  |  |
|**creditsUsed** | **Integer** | Text credits only. 0 while the image credit pool is on; &#x60;count × credit_weight&#x60; when it is switched off. |  |
|**creditsRemaining** | **Integer** | Text credits left this billing cycle (null &#x3D; no limit). |  [optional] |
|**imageCreditsUsed** | **Integer** | Image credits this call spent (1 per image; 0 when the image credit pool is switched off). |  |
|**imageCreditsRemaining** | **Integer** | Image credits left this month (null &#x3D; no limit, or the image credit pool is switched off). |  |



