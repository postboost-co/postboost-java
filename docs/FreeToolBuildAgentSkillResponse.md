

# FreeToolBuildAgentSkillResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**format** | [**FormatEnum**](#FormatEnum) |  |  [optional] |
|**filename** | [**FilenameEnum**](#FilenameEnum) |  |  [optional] |
|**content** | **String** | The file, in Markdown. |  [optional] |
|**install** | **List&lt;String&gt;** | Where to put the file. |  [optional] |
|**toolsUsed** | **List&lt;String&gt;** | The connector tool names the content names, in first-appearance order; empty with api_token. |  [optional] |
|**lines** | **Integer** |  |  [optional] |
|**warnings** | [**List&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: name_normalized, task_limited_by_autonomy, autonomy_high, too_long. |  [optional] |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| SKILL_MD | &quot;skill_md&quot; |
| AGENTS_MD | &quot;agents_md&quot; |
| SYSTEM_PROMPT | &quot;system_prompt&quot; |



## Enum: FilenameEnum

| Name | Value |
|---- | -----|
| SKILL_MD | &quot;SKILL.md&quot; |
| AGENTS_MD | &quot;AGENTS.md&quot; |
| SYSTEM_PROMPT_MD | &quot;system-prompt.md&quot; |



