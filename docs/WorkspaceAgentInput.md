

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
| FAILED_POST_FIXER | &quot;failed_post_fixer&quot; |



## Enum: ScheduleEnum

| Name | Value |
|---- | -----|
| HOURLY | &quot;hourly&quot; |
| EVERY_6_HOURS | &quot;every_6_hours&quot; |
| DAILY | &quot;daily&quot; |
| WEEKLY | &quot;weekly&quot; |



