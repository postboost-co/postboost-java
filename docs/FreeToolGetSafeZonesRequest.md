

# FreeToolGetSafeZonesRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**platform** | [**PlatformEnum**](#PlatformEnum) | The app the vertical video is posted to. Approximate: platforms do not publish official overlay sizes for organic posts, and the UI varies by device and app version. The boxes come from each platform&#39;s guidance for vertical video ads. Sources last verified 2026-10-19. |  |
|**width** | **Integer** | Frame width in pixels. The boxes are measured on 1080 × 1920 and scaled to the frame. |  [optional] |
|**height** | **Integer** | Frame height in pixels. |  [optional] |



## Enum: PlatformEnum

| Name | Value |
|---- | -----|
| TIKTOK | &quot;tiktok&quot; |
| INSTAGRAM_REELS | &quot;instagram_reels&quot; |
| YOUTUBE_SHORTS | &quot;youtube_shorts&quot; |



