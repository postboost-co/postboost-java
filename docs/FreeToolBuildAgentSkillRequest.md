

# FreeToolBuildAgentSkillRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**format** | [**FormatEnum**](#FormatEnum) | skill_md (an Agent Skills SKILL.md), agents_md (AGENTS.md) or system_prompt. |  [optional] |
|**name** | **String** | The skill name, normalised to lowercase letters, digits and hyphens and cut to 64 characters. |  [optional] |
|**brand** | **String** | The brand the agent works for; omitted when empty. |  [optional] |
|**tasks** | [**Set&lt;TasksEnum&gt;**](#Set&lt;TasksEnum&gt;) | What the agent does; the output keeps this enum&#39;s order. |  [optional] |
|**networks** | [**Set&lt;NetworksEnum&gt;**](#Set&lt;NetworksEnum&gt;) | Networks to add character-limit rules for; none leaves the section out. |  [optional] |
|**autonomy** | [**AutonomyEnum**](#AutonomyEnum) | How much the agent may do without asking. |  [optional] |
|**dailyCap** | **Integer** | Posts per day the agent may create; 0 adds no cap line. |  [optional] |
|**brandVoice** | **Boolean** | Read the workspace brand voice before writing captions. |  [optional] |
|**connection** | [**ConnectionEnum**](#ConnectionEnum) | connector (the OAuth MCP connector) or api_token (the advanced MCP server with an API key). |  [optional] |
|**rules** | **List&lt;String&gt;** | Your own do&#39;s and don&#39;ts, one per item. |  [optional] |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| SKILL_MD | &quot;skill_md&quot; |
| AGENTS_MD | &quot;agents_md&quot; |
| SYSTEM_PROMPT | &quot;system_prompt&quot; |



## Enum: Set&lt;TasksEnum&gt;

| Name | Value |
|---- | -----|
| DRAFT_POSTS | &quot;draft_posts&quot; |
| SCHEDULE_POSTS | &quot;schedule_posts&quot; |
| REPURPOSE | &quot;repurpose&quot; |
| ANALYTICS | &quot;analytics&quot; |
| FAILED_POSTS | &quot;failed_posts&quot; |
| AUTOMATIONS | &quot;automations&quot; |
| AGENT_PROPOSALS | &quot;agent_proposals&quot; |



## Enum: Set&lt;NetworksEnum&gt;

| Name | Value |
|---- | -----|
| X | &quot;x&quot; |
| THREADS | &quot;threads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| INSTAGRAM | &quot;instagram&quot; |
| FACEBOOK | &quot;facebook&quot; |
| TIKTOK | &quot;tiktok&quot; |
| PINTEREST | &quot;pinterest&quot; |
| YOUTUBE | &quot;youtube&quot; |
| GBP | &quot;gbp&quot; |



## Enum: AutonomyEnum

| Name | Value |
|---- | -----|
| DRAFTS_ONLY | &quot;drafts_only&quot; |
| APPROVE_THEN_SCHEDULE | &quot;approve_then_schedule&quot; |
| QUEUE_WITHOUT_ASKING | &quot;queue_without_asking&quot; |



## Enum: ConnectionEnum

| Name | Value |
|---- | -----|
| CONNECTOR | &quot;connector&quot; |
| API_TOKEN | &quot;api_token&quot; |



