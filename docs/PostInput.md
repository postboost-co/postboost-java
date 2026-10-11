

# PostInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**versions** | [**List&lt;PostVersion&gt;**](PostVersion.md) | At least one version with &#x60;is_original: true&#x60; is required. |  |
|**accounts** | **List&lt;Integer&gt;** | Account IDs to publish to. |  [optional] |
|**tags** | **List&lt;Integer&gt;** | Tag IDs to attach. |  [optional] |
|**date** | **LocalDate** |  |  [optional] |
|**time** | **String** |  |  [optional] |
|**timezone** | **String** | Timezone &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in. Defaults to the workspace timezone. |  [optional] |
|**accountsSchedule** | [**List&lt;AccountSchedule&gt;**](AccountSchedule.md) | Per-account departure times. When omitted on update, accounts keep their offsets from the post time. |  [optional] |
|**schedule** | **Boolean** | Schedule the post for the given date/time. |  [optional] |
|**scheduleNow** | **Boolean** | Publish immediately. |  [optional] |
|**queue** | **Boolean** | Add to the smart publishing queue. |  [optional] |



