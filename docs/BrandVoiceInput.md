

# BrandVoiceInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**businessName** | **String** |  |  [optional] |
|**mission** | **String** |  |  [optional] |
|**industry** | **String** |  |  [optional] |
|**personality** | **String** | How the brand sounds. The first sentence also feeds image prompts. |  [optional] |
|**audience** | **List&lt;String&gt;** |  |  [optional] |
|**topicsPreferred** | **List&lt;String&gt;** |  |  [optional] |
|**topicsAvoided** | **List&lt;String&gt;** |  |  [optional] |
|**toneFormal** | **Integer** | 1 very casual, 3 neutral, 5 very formal. |  [optional] |
|**tonePlayful** | **Integer** | 1 strictly serious, 3 neutral, 5 very playful. |  [optional] |
|**toneTechnical** | **Integer** | 1 very simple, 3 neutral, 5 highly technical. |  [optional] |
|**emojiStyle** | [**EmojiStyleEnum**](#EmojiStyleEnum) |  |  [optional] |
|**hashtagStrategy** | [**HashtagStrategyEnum**](#HashtagStrategyEnum) |  |  [optional] |
|**avoidWords** | **List&lt;String&gt;** |  |  [optional] |
|**preferredCta** | **List&lt;String&gt;** |  |  [optional] |
|**examplePosts** | **List&lt;String&gt;** |  |  [optional] |



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



