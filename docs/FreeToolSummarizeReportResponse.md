

# FreeToolSummarizeReportResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**posts** | **Integer** |  |  [optional] |
|**dateRange** | [**FreeToolSummarizeReportResponseDateRange**](FreeToolSummarizeReportResponseDateRange.md) |  |  [optional] |
|**views** | **Integer** |  |  [optional] |
|**engagements** | **Integer** |  |  [optional] |
|**engagementRate** | **BigDecimal** | Percent, 2 decimals; null without views. |  [optional] |
|**engagementsFrom** | **List&lt;String&gt;** | The counts added up as engagements. |  [optional] |
|**networks** | [**List&lt;FreeToolSummarizeReportResponseNetworksInner&gt;**](FreeToolSummarizeReportResponseNetworksInner.md) |  |  [optional] |
|**topPosts** | [**List&lt;FreeToolSummarizeReportResponseTopPostsInner&gt;**](FreeToolSummarizeReportResponseTopPostsInner.md) |  |  [optional] |
|**weekdays** | [**List&lt;FreeToolSummarizeReportResponseWeekdaysInner&gt;**](FreeToolSummarizeReportResponseWeekdaysInner.md) |  |  [optional] |
|**bestWeekday** | **String** | The weekday with the highest average engagements per post. |  [optional] |



