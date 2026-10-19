

# FreeToolFindAutomationRecipesResponseRecipesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**slug** | **String** | Stable key of the recipe, also its anchor on the page. |  [optional] |
|**title** | **String** | What the recipe does. |  [optional] |
|**trigger** | [**TriggerEnum**](#TriggerEnum) | What starts it. |  [optional] |
|**goal** | **String** | The result in one or two sentences. |  [optional] |
|**_native** | [**FreeToolFindAutomationRecipesResponseRecipesInnerNative**](FreeToolFindAutomationRecipesResponseRecipesInnerNative.md) |  |  [optional] |
|**apiOperations** | [**List&lt;FreeToolFindAutomationRecipesResponseRecipesInnerApiOperationsInner&gt;**](FreeToolFindAutomationRecipesResponseRecipesInnerApiOperationsInner.md) | The PostBoost API operations the recipe calls. |  [optional] |
|**steps** | [**FreeToolFindAutomationRecipesResponseRecipesInnerSteps**](FreeToolFindAutomationRecipesResponseRecipesInnerSteps.md) |  |  [optional] |
|**n8nWorkflow** | **Map&lt;String, Object&gt;** | Importable n8n workflow (core nodes only; add a Header Auth credential named \&quot;PostBoost API token\&quot;) when &#x60;platform&#x60; is &#x60;n8n&#x60;; null otherwise. |  [optional] |



## Enum: TriggerEnum

| Name | Value |
|---- | -----|
| RSS | &quot;rss&quot; |
| SPREADSHEET | &quot;spreadsheet&quot; |
| FILE | &quot;file&quot; |
| APPROVAL | &quot;approval&quot; |
| WEBHOOK | &quot;webhook&quot; |
| SCHEDULE | &quot;schedule&quot; |



