

# PostInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**versions** | [**List&lt;PostVersion&gt;**](PostVersion.md) | At least one version with &#x60;is_original: true&#x60; is required. |  |
|**accounts** | **List&lt;Integer&gt;** | Account IDs to publish to. |  [optional] |
|**tags** | **List&lt;Integer&gt;** | Tag IDs to attach. |  [optional] |
|**date** | **LocalDate** |  |  [optional] |
|**time** | **String** |  |  [optional] |
|**timezone** | **String** |  |  [optional] |
|**schedule** | **Boolean** | Schedule the post for the given date/time. |  [optional] |
|**scheduleNow** | **Boolean** | Publish immediately. |  [optional] |
|**queue** | **Boolean** | Add to the smart publishing queue. |  [optional] |



