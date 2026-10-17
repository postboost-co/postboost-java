

# FreeToolPlanPostingFrequencyResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**postsPerWeekCapacity** | **Integer** |  |  [optional] |
|**sumOfMinimums** | **Integer** | The recommended minimums of the chosen networks added up. |  [optional] |
|**networks** | [**List&lt;FreeToolPlanPostingFrequencyResponseNetworksInner&gt;**](FreeToolPlanPostingFrequencyResponseNetworksInner.md) | One row per chosen network, in a fixed network order. |  [optional] |
|**slots** | [**List&lt;FreeToolPlanPostingFrequencyResponseSlotsInner&gt;**](FreeToolPlanPostingFrequencyResponseSlotsInner.md) | The weekly grid: each network&#39;s posts spread evenly from Monday, sorted by day. |  [optional] |
|**warnings** | **List&lt;String&gt;** |  |  [optional] |
|**lastVerified** | **LocalDate** | When the ranges were last checked against their sources. |  [optional] |



