

# BrandVoice


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**businessName** | **String** |  |  [optional] |
|**mission** | **String** |  |  [optional] |
|**industry** | **String** |  |  [optional] |
|**personality** | **String** |  |  [optional] |
|**audience** | **List&lt;String&gt;** |  |  [optional] |
|**topicsPreferred** | **List&lt;String&gt;** |  |  [optional] |
|**topicsAvoided** | **List&lt;String&gt;** |  |  [optional] |
|**toneFormal** | **Integer** |  |  |
|**tonePlayful** | **Integer** |  |  |
|**toneTechnical** | **Integer** |  |  |
|**emojiStyle** | [**EmojiStyleEnum**](#EmojiStyleEnum) |  |  |
|**hashtagStrategy** | [**HashtagStrategyEnum**](#HashtagStrategyEnum) |  |  |
|**avoidWords** | **List&lt;String&gt;** |  |  [optional] |
|**preferredCta** | **List&lt;String&gt;** |  |  [optional] |
|**examplePosts** | **List&lt;String&gt;** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



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



