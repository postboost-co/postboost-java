

# PostingTimes


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**hasData** | **Boolean** |  |  |
|**timezone** | **String** |  |  |
|**offsetHours** | **Integer** |  |  |
|**accounts** | **Integer** | Accounts that contributed scores. |  |
|**samples** | **Integer** |  |  |
|**days** | [**List&lt;PostingTimesDaysInner&gt;**](PostingTimesDaysInner.md) | One entry per weekday (&#x60;day&#x60; 0 &#x3D; Sunday). |  |
|**dayIntervals** | **List&lt;List&lt;PostingTimesDayIntervalsInnerInner&gt;&gt;** | Per weekday, 2-hour intervals. |  |
|**best** | [**List&lt;PostingTimesBestInner&gt;**](PostingTimesBestInner.md) | Up to three recommended slots, at most one per weekday. |  |



