

# PostVersionOptions

Platform-specific publishing options, keyed by network (`tiktok`, `youtube`, `instagram`, `mastodon`, …). Options of networks the post does not publish to are ignored. To label a post as AI-generated on every network that supports it, send `ai_generated` on the post instead of setting `tiktok.is_aigc`, `youtube.contains_synthetic_media` or `instagram.ai_generated` yourself. 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**tiktok** | [**PostOptionsTikTok**](PostOptionsTikTok.md) |  |  [optional] |
|**youtube** | [**PostOptionsYoutube**](PostOptionsYoutube.md) |  |  [optional] |
|**instagram** | [**PostOptionsInstagram**](PostOptionsInstagram.md) |  |  [optional] |
|**instagramStandalone** | [**PostOptionsInstagram**](PostOptionsInstagram.md) |  |  [optional] |



