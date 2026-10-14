

# WorkspaceAgentSettings

Agent settings; each type reads its own keys. Pre-publish checker: `horizon_hours`, `check_links`, `banned_phrases`, `ai_review`, `max_ai_reviews_per_run`. Failed-post fixer: `lookback_hours`. 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**horizonHours** | **Integer** | Check posts scheduled within this many hours. |  [optional] |
|**checkLinks** | **Boolean** | Flag links in captions that answer an HTTP error. |  [optional] |
|**bannedPhrases** | **List&lt;String&gt;** | Phrases to propose removing from captions. |  [optional] |
|**aiReview** | **Boolean** | Ask AI to review captions (one AI credit per reviewed post). |  [optional] |
|**maxAiReviewsPerRun** | **Integer** |  |  [optional] |
|**lookbackHours** | **Integer** | Look at posts that failed within this many hours. |  [optional] |



