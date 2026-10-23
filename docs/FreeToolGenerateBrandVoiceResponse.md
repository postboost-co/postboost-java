

# FreeToolGenerateBrandVoiceResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**voice** | [**FreeToolGenerateBrandVoiceResponseVoice**](FreeToolGenerateBrandVoiceResponseVoice.md) |  |  [optional] |
|**evidence** | **Map&lt;String, List&lt;String&gt;&gt;** | Per trait key, up to 2 quotes from your posts that show it; only quotes found in your posts are kept, so a list can be empty. |  [optional] |
|**systemPrompt** | **String** | The system prompt PostBoost&#39;s AI uses for this voice; paste it into ChatGPT, Claude or your agent. |  [optional] |
|**markdown** | **String** | The voice as a Markdown guide with its quotes, ending with the system prompt. |  [optional] |
|**creditsSpent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. |  [optional] |
|**cached** | **Boolean** | True when the same request was answered before (free). |  [optional] |



