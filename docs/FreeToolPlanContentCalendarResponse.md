

# FreeToolPlanContentCalendarResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**endDate** | **String** | Last day of the calendar (YYYY-MM-DD). |  [optional] |
|**total** | **Integer** | Number of posts planned. |  [optional] |
|**slots** | [**List&lt;FreeToolPlanContentCalendarResponseSlotsInner&gt;**](FreeToolPlanContentCalendarResponseSlotsInner.md) |  |  [optional] |
|**csv** | **String** | The calendar as CSV (UTF-8 with BOM): Date, Day, Time, Network, Pillar, Idea. |  [optional] |
|**ics** | **String** | The calendar as an iCalendar file: one 15-minute event per post, in floating local time. |  [optional] |



