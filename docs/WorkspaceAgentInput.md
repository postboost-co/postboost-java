

# WorkspaceAgentInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) |  |  |
|**name** | **String** |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**schedule** | [**ScheduleEnum**](#ScheduleEnum) |  |  [optional] |
|**settings** | [**WorkspaceAgentSettings**](WorkspaceAgentSettings.md) |  |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| PRE_PUBLISH_CHECKER | &quot;pre_publish_checker&quot; |



## Enum: ScheduleEnum

| Name | Value |
|---- | -----|
| HOURLY | &quot;hourly&quot; |
| EVERY_6_HOURS | &quot;every_6_hours&quot; |
| DAILY | &quot;daily&quot; |
| WEEKLY | &quot;weekly&quot; |



