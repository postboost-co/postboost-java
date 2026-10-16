

# FreeToolPreviewPostResponseNetworksInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**key** | [**KeyEnum**](#KeyEnum) |  |  [optional] |
|**count** | **Integer** |  |  [optional] |
|**limit** | **Integer** |  |  [optional] |
|**over** | **Boolean** |  |  [optional] |
|**preview** | **String** | What the feed shows before the \&quot;more\&quot; link (approximate; varies by device). |  [optional] |
|**folded** | **Boolean** |  |  [optional] |
|**minRatio** | **String** | Tallest image ratio the feed shows uncropped (Instagram: the chosen ratio). Taller images are cropped from the centre. |  [optional] |
|**maxRatio** | **String** | Widest image ratio the feed shows uncropped (Instagram: the chosen ratio). Wider images are cropped from the centre. |  [optional] |
|**displayRatio** | **BigDecimal** | Width / height the card shows the image at, 2 decimals. Only when image_width and image_height are given. |  [optional] |
|**cropped** | **Boolean** | Whether the card crops the image. Only when image_width and image_height are given. |  [optional] |



## Enum: KeyEnum

| Name | Value |
|---- | -----|
| INSTAGRAM | &quot;instagram&quot; |
| X | &quot;x&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| FACEBOOK | &quot;facebook&quot; |



