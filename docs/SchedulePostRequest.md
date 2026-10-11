

# SchedulePostRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**postNow** | **Boolean** |  |  |
|**date** | **LocalDate** | New date for the post (Y-m-d). Use together with &#x60;time&#x60;. |  [optional] |
|**time** | **String** | New time for the post (H:i). |  [optional] |
|**timezone** | **String** | Timezone &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in. Defaults to the workspace timezone. |  [optional] |
|**accountsSchedule** | [**List&lt;AccountSchedule&gt;**](AccountSchedule.md) | Per-account departure times. When omitted, accounts keep their offsets from the post time. |  [optional] |



