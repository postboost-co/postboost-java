

# FreeToolGenerateSocialPostsFromVideoResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**outputs** | [**FreeToolGenerateSocialPostsFromVideoResponseOutputs**](FreeToolGenerateSocialPostsFromVideoResponseOutputs.md) |  |  [optional] |
|**outputsSkipped** | **List&lt;String&gt;** | Requested outputs that came back empty: generate again to get them. |  [optional] |
|**warnings** | **List&lt;String&gt;** | What to know before posting, in plain words. |  [optional] |
|**videoUrl** | **String** | The normalised video link the posts use, or null. |  [optional] |
|**cleanedChars** | **Integer** | Characters of caption text left after cleaning; the model read these. |  [optional] |
|**removedTimestamps** | **Boolean** | True when timestamps, cue numbers, tags or repeated caption lines were removed. |  [optional] |
|**creditsSpent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. |  [optional] |
|**cached** | **Boolean** | True when the same request was answered before (free). |  [optional] |



