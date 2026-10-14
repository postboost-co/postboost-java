

# FreeToolCalculateEngagementRateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**likes** | **Integer** |  |  [optional] |
|**comments** | **Integer** |  |  [optional] |
|**shares** | **Integer** |  |  [optional] |
|**saves** | **Integer** |  |  [optional] |
|**clicks** | **Integer** |  |  [optional] |
|**method** | [**MethodEnum**](#MethodEnum) | What to divide by. |  [optional] |
|**base** | **Integer** | Followers, or the total reach or impressions of the posts. |  |
|**posts** | **Integer** | Number of posts the engagements come from. |  [optional] |



## Enum: MethodEnum

| Name | Value |
|---- | -----|
| FOLLOWERS | &quot;followers&quot; |
| REACH | &quot;reach&quot; |
| IMPRESSIONS | &quot;impressions&quot; |



