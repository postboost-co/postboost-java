

# FreeToolCalculateCarouselSlicesResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**slides** | [**List&lt;FreeToolCalculateCarouselSlicesResponseSlidesInner&gt;**](FreeToolCalculateCarouselSlicesResponseSlidesInner.md) | The part of the source image each slide shows, left to right, in source pixels. |  [optional] |
|**output** | [**FreeToolCalculateCarouselSlicesResponseOutput**](FreeToolCalculateCarouselSlicesResponseOutput.md) |  |  [optional] |
|**scale** | **BigDecimal** | Output pixels per source pixel, 4 decimals. |  [optional] |
|**upscaled** | **Boolean** | True when the source is enlarged (scale above 1), which can look soft. |  [optional] |
|**warnings** | **List&lt;String&gt;** | Upscaling and how much of the source is cropped away. |  [optional] |



