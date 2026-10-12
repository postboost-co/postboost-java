

# PostingSchedule


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**accountId** | **Integer** | The account asked for; 0 for the workspace schedule. |  |
|**sourceAccountId** | **Integer** | Whose schedule applies; 0 when the workspace schedule applies. |  |
|**inherited** | **Boolean** | True when the account follows the workspace schedule. |  |
|**timezone** | **String** |  |  |
|**autoTune** | **Boolean** | Adjust times automatically from engagement data. |  |
|**times** | [**List&lt;PostingScheduleDay&gt;**](PostingScheduleDay.md) |  |  |



