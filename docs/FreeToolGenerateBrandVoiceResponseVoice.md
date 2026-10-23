

# FreeToolGenerateBrandVoiceResponseVoice

The voice in PostBoost's brand voice format (the workspace brand voice fields).

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**businessName** | **String** | Your input, or null. |  [optional] |
|**mission** | **String** | Only when the posts state it, else null. |  [optional] |
|**industry** | **String** | Your input, or null. |  [optional] |
|**personality** | **String** | How the brand sounds. |  [optional] |
|**audience** | **List&lt;String&gt;** | Who the posts speak to. At most 8 items. |  [optional] |
|**topicsPreferred** | **List&lt;String&gt;** | Topics the posts come back to. At most 8 items. |  [optional] |
|**topicsAvoided** | **List&lt;String&gt;** | Topics the posts clearly steer away from; often empty. At most 8 items. |  [optional] |
|**toneFormal** | **Integer** | 1 very casual to 5 very formal, 3 neutral. |  [optional] |
|**tonePlayful** | **Integer** | 1 very serious to 5 very playful, 3 neutral. |  [optional] |
|**toneTechnical** | **Integer** | 1 very simple to 5 very technical, 3 neutral. |  [optional] |
|**emojiStyle** | [**EmojiStyleEnum**](#EmojiStyleEnum) |  |  [optional] |
|**hashtagStrategy** | [**HashtagStrategyEnum**](#HashtagStrategyEnum) |  |  [optional] |
|**avoidWords** | **List&lt;String&gt;** | Words the posts clearly avoid; often empty. At most 8 items. |  [optional] |
|**preferredCta** | **List&lt;String&gt;** | Calls to action the posts use. At most 8 items. |  [optional] |
|**examplePosts** | **List&lt;String&gt;** | Up to 5 of your posts that sound most typical, exactly as given. |  [optional] |



## Enum: EmojiStyleEnum

| Name | Value |
|---- | -----|
| NONE | &quot;none&quot; |
| RARE | &quot;rare&quot; |
| MODERATE | &quot;moderate&quot; |
| ABUNDANT | &quot;abundant&quot; |



## Enum: HashtagStrategyEnum

| Name | Value |
|---- | -----|
| NONE | &quot;none&quot; |
| GENERIC | &quot;generic&quot; |
| NICHE | &quot;niche&quot; |
| BRANDED | &quot;branded&quot; |
| MIX | &quot;mix&quot; |



